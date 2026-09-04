Add gradient support for multi-dimensional `wp.indexedarray` kernel inputs. Gradients previously worked only for 1-D
indexed arrays (`NotImplementedError` for higher ranks); the adjoint now follows the per-dimension gather indirection
for 2-D, 3-D, and 4-D indexed arrays, including views that mix indexed and passthrough dimensions.

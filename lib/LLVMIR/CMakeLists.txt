add_llvm_library(MLIRLLVMIR
  Transforms/ConvertToLLVMDialect.cpp
  IR/LLVMDialect.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/LLVMIR
  )
add_dependencies(MLIRLLVMIR MLIRLLVMOpsIncGen MLIRLLVMConversionsIncGen LLVMAsmParser LLVMCore LLVMSupport)
target_link_libraries(MLIRLLVMIR LLVMAsmParser LLVMCore LLVMSupport)

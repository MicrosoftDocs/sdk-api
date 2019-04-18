---
UID: NS:directml.DML_BUFFER_TENSOR_DESC
title: DML_BUFFER_TENSOR_DESC
author: windows-sdk-content
description: Describes a tensor that will be stored in a Direct3D 12 buffer resource.
old-location: direct3d12\dml_buffer_tensor_desc.htm
tech.root: direct3d12
ms.assetid: 03EAFF60-1703-47BA-BD77-225BEAC4DFAE
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DML_BUFFER_TENSOR_DESC, DML_BUFFER_TENSOR_DESC structure, direct3d12.dml_buffer_tensor_desc, directml/DML_BUFFER_TENSOR_DESC
ms.topic: struct
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_BUFFER_TENSOR_DESC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DML_BUFFER_TENSOR_DESC structure


## -description






Describes a tensor that will be stored in a Direct3D 12 buffer resource. The corresponding tensor type is [DML_TENSOR_TYPE_BUFFER](/windows/desktop/api/directml/ne-directml-dml_tensor_type), and the corresponding binding type is
    [DML_BINDING_TYPE_BUFFER](/windows/desktop/api/directml/ne-directml-dml_binding_type).


## -struct-fields




### -field DataType

Type: [**DML_TENSOR_DATA_TYPE**](/windows/desktop/api/directml/ne-directml-dml_tensor_data_type)

The type of the values in the tensor.


### -field Flags

Type: [**DML_TENSOR_FLAGS**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags)

Specifies additional options for the tensor.


### -field DimensionCount

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The number of dimensions of the tensor. This field determines the size of the <i>Sizes</i> and <i>Strides</i> arrays (if provided).


### -field Sizes

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

The size, in elements, of each dimension in the tensor. Specifying a size of zero in any dimension is
      invalid, and will result in an error.


### -field Strides

Type: <b>const [UINT](/windows/desktop/winprog/windows-data-types)*</b>

Optional. Determines the number of elements (not bytes) to linearly traverse in order to reach the next element
      in that dimension. For example, a stride of 5 in dimension 1 means that the distance between elements (n) and
      (n+1) in that dimension is 5 elements when traversing the buffer linearly.

<i>Strides</i> can be used to express broadcasting (by specifying a stride of 0) as well as padding (for example, by using a
      stride larger than the physical size of a row, to pad the end of a row).

If <i>Strides</i> is not specified, each dimension in the tensor is considered to be contiguously packed, with no
      additional padding.


### -field TotalTensorSizeInBytes

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT64</a></b>

Defines a minimum size in bytes for the buffer that will contain this tensor. <i>TotalTensorSizeInBytes</i> must
      be at least as large as the minimum implied size given the sizes, strides, and data type of the tensor. You can calculate the minimum implied size by calling the [DMLCalcBufferTensorSize](/windows/desktop/direct3d12/dml-helper-functions#dmlcalcbuffertensorsize) utility free function.

Providing a <i>TotalTensorSizeInBytes</i> that is larger than the minimum implied size may enable additional
      optimizations by allowing DirectML to elide bounds checking in some cases if the <i>TotalTensorSizeInBytes</i> defines
      sufficient padding beyond the end of the tensor data.

When binding this tensor, the size of the buffer range must be at least as large as the <i>TotalTensorSizeInBytes</i>.
      For output tensors, this has the additional effect of permitting DirectML to write to any memory within the
      <i>TotalTensorSizeInBytes</i>. That is, your application mustn't assume that DirectML will preserve any padding bytes
      inside output tensors that are inside the <i>TotalTensorSizeInBytes</i>.

The total size of a buffer tensor may not exceed (2^32 - 1) elements—for example, 16GB for a <b>FLOAT32</b> tensor.



### -field GuaranteedBaseOffsetAlignment

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

Optional. Defines a minimum guaranteed alignment in bytes for the base offset of the buffer range that will
      contain this tensor, or 0 to provide no minimum guaranteed alignment. If specified, this value must be a power
      of two that is at least as large as the element size.

When binding this tensor, the offset in bytes of the buffer range from the start of the buffer must be a multiple
      of the <i>GuaranteedBaseOffsetAlignment</i>, if provided.

Buffer tensors always have a minimum alignment of 16 bytes. However, providing a larger value for the
      <i>GuaranteedBaseOffsetAlignment</i> may allow DirectML to achieve better performance, because a larger alignment enables
      the use of vectorized load/store instructions.

Although this field is optional, for best performance we recommend that you align tensors to boundaries of 32
      bytes or more, where possible.


## -see-also




<a href="/windows/desktop/direct3d12/dml-binding">Binding in DirectML</a>
 

 


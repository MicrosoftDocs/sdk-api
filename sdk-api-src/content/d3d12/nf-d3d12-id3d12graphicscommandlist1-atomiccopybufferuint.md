---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ID3D12GraphicsCommandList1::AtomicCopyBufferUINT


## -description


Atomically copies a primary data element of type UINT from one resource to another, along with optional dependent resources.

These 'dependent resourses' are so-named because they depend upon the primary data element to locate them, typically the key element is an address, index, or other handle that refers to one or more the dependent resources indirectly. 

This function supports a primary data element of type UINT (32bit). A different version of this function, <a href="https://msdn.microsoft.com/F83870E9-5256-4A3E-BAF7-05C4CCB28442">AtomicCopyBufferUINT64</a>, supports a primary data element of type UINT64 (64bit).


## -parameters




### -param pDstBuffer [in]

Type: <b>ID3D12Resource*</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_In_</code>

The resource that the UINT primary data element is copied into.


### -param DstOffset

Type: <b>UINT64</b>

An offset into the destination resource buffer that specifies where the primary data element is copied into, in bytes. This offset combined with the base address of the resource buffer must result in a memory address that's naturally aligned for UINT values.


### -param pSrcBuffer [in]

Type: <b>ID3D12Resource*</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_In_</code>

The resource that the UINT primary data element is copied from. This data is typically an address, index, or other handle that shader code can use to locate the most-recent version of latency-sensitive information.


### -param SrcOffset

Type: <b>UINT64</b>

An offset into the source resource buffer that specifies where the primary data element is copied from, in bytes. This offset combined with the base address of the resource buffer must result in a memory address that's naturally aligned for UINT values.


### -param Dependencies

Type: <b>UINT</b>

The number of dependent resources.


### -param ppDependentResources [in]

Type: <b>ID3D12Resource*</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_In_reads_(Dependencies)</code>

An array of resources that contain the dependent elements of the data payload.


### -param pDependentSubresourceRanges [in]

Type: <b>const <a href="https://msdn.microsoft.com/D8DACE22-9AFD-4DCD-A254-A34AD532ACD7">D3D12_SUBRESOURCE_RANGE_UINT64</a>*</b>

<a href="https://msdn.microsoft.com/en-us/library/hh916382.aspx">SAL</a>: <code>_In_reads_(Dependencies)</code>

An array of subresource ranges that specify the dependent elements of the data payload. These elements are completely updated before the primary data element is itself atomically copied. This ensures that the entire operation is logically atomic; that is, the primary data element never refers to an incomplete data payload.


## -returns



This method does not return a value.




## -remarks



This method is typically used to update resources for which normal rendering pipeline latency can be detrimental to user experience. For example, an application can compute a view matrix from the latest user input (such as from the sensors of a head-mounted display), and use this function to update and activate this matrix in command lists already dispatched to the GPU to reduce percieved latency between input and rendering.




## -see-also




<a href="https://msdn.microsoft.com/E156C26B-0E51-4F43-9AB2-373E4C67A496">ID3D12GraphicsCommandList1</a>
 

 


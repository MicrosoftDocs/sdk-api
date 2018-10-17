---
UID: NF:mfidl.MFSerializePresentationDescriptor
title: MFSerializePresentationDescriptor function
author: windows-sdk-content
description: Serializes a presentation descriptor to a byte array.
old-location: mf\mfserializepresentationdescriptor.htm
tech.root: medfound
ms.assetid: f39a0dc8-438e-4723-94e4-a194a0a460e3
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: MFSerializePresentationDescriptor, MFSerializePresentationDescriptor function [Media Foundation], f39a0dc8-438e-4723-94e4-a194a0a460e3, mf.mfserializepresentationdescriptor, mfidl/MFSerializePresentationDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFSerializePresentationDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFSerializePresentationDescriptor function


## -description



Serializes a presentation descriptor to a byte array.




## -parameters




### -param pPD

Pointer to the <a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a> interface of the presentation descriptor to serialize.


### -param pcbData

Receives the size of the <i>ppbData</i> array, in bytes.


### -param ppbData

Receives a pointer to an array of bytes containing the serialized presentation descriptor. The caller must free the memory for the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



To deserialize the presentation descriptor, pass the byte array to the <a href="https://msdn.microsoft.com/4f567b86-bce2-49fe-9d43-d1dfa57a86cb">MFDeserializePresentationDescriptor</a> function.




## -see-also




<a href="https://msdn.microsoft.com/db03e212-7021-433e-84dc-410b2cf7af87">IMFPresentationDescriptor</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 


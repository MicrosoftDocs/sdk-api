---
UID: NF:mfidl.MFDeserializePresentationDescriptor
title: MFDeserializePresentationDescriptor function (mfidl.h)
author: windows-sdk-content
description: Deserializes a presentation descriptor from a byte array.
old-location: mf\mfdeserializepresentationdescriptor.htm
tech.root: medfound
ms.assetid: 4f567b86-bce2-49fe-9d43-d1dfa57a86cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 4f567b86-bce2-49fe-9d43-d1dfa57a86cb, MFDeserializePresentationDescriptor, MFDeserializePresentationDescriptor function [Media Foundation], mf.mfdeserializepresentationdescriptor, mfidl/MFDeserializePresentationDescriptor
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
 - MFDeserializePresentationDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFDeserializePresentationDescriptor function


## -description



Deserializes a presentation descriptor from a byte array.




## -parameters




### -param cbData

Size of the <i>pbData</i> array, in bytes.


### -param pbData

Pointer to an array of bytes that contains the serialized presentation descriptor.


### -param ppPD

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor">IMFPresentationDescriptor</a> interface of the presentation descriptor. The caller must release the interface.


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-mfserializepresentationdescriptor">MFSerializePresentationDescriptor</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 


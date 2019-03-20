---
UID: NF:mfapi.MFCreateMediaTypeFromRepresentation
title: MFCreateMediaTypeFromRepresentation function (mfapi.h)
author: windows-sdk-content
description: Creates a Media Foundation media type from another format representation.
old-location: mf\mfcreatemediatypefromrepresentation.htm
tech.root: medfound
ms.assetid: 5d85c47e-2e40-45f2-8f17-52f642652112
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 5d85c47e-2e40-45f2-8f17-52f642652112, MFCreateMediaTypeFromRepresentation, MFCreateMediaTypeFromRepresentation function [Media Foundation], mf.mfcreatemediatypefromrepresentation, mfapi/MFCreateMediaTypeFromRepresentation
ms.topic: function
req.header: mfapi.h
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
 - MFCreateMediaTypeFromRepresentation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateMediaTypeFromRepresentation function


## -description



Creates a Media Foundation media type from another format representation.




## -parameters




### -param guidRepresentation [in]

GUID that specifies which format representation to convert. The following value is defined.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td>AM_MEDIA_TYPE_REPRESENTATION</td>
<td>Convert a DirectShow <b>AM_MEDIA_TYPE</b> structure.</td>
</tr>
</table>
 


### -param pvRepresentation [in]

Pointer to a buffer that contains the format representation to convert. The layout of the buffer depends on the value of <i>guidRepresentation</i>.


### -param ppIMediaType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the interface.


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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_REPRESENTATION</b></dt>
</dl>
</td>
<td width="60%">
The GUID specified in <i>guidRepresentation</i> is not supported.

</td>
</tr>
</table>
 




## -remarks



If the original format is a DirectShow audio media type, and the format type is not recognized, the function sets the following attributes on the converted media type.

<table>
<tr>
<th>Attribute</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/dc532791-39e1-4acb-9e62-21d8f25be870">MF_MT_AM_FORMAT_TYPE</a>
</td>
<td>Contains the format type GUID.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/020832c4-40a1-4d8b-ada0-7a04ce097bce">MF_MT_USER_DATA</a>
</td>
<td>Contains the format block.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 


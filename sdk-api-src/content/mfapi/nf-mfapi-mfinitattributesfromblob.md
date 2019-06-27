---
UID: NF:mfapi.MFInitAttributesFromBlob
title: MFInitAttributesFromBlob function (mfapi.h)
author: windows-sdk-content
description: Initializes the contents of an attribute store from a byte array.
old-location: mf\mfinitattributesfromblob.htm
tech.root: medfound
ms.assetid: da0f01a3-ed47-42a1-b4af-5f3cbc9271a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFInitAttributesFromBlob, MFInitAttributesFromBlob function [Media Foundation], da0f01a3-ed47-42a1-b4af-5f3cbc9271a3, mf.mfinitattributesfromblob, mfapi/MFInitAttributesFromBlob
ms.topic: function
f1_keywords: 
 - "mfapi/MFInitAttributesFromBlob"
req.header: mfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - MFInitAttributesFromBlob
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFInitAttributesFromBlob function


## -description



Initializes the contents of an attribute store from a byte array.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.


### -param pBuf [in]

Pointer to the array that contains the initialization data.


### -param cbBufSize [in]

Size of the <i>pBuf</i> array, in bytes.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not valid.

</td>
</tr>
</table>
 




## -remarks



Use this function to deserialize an attribute store that was serialized with the <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob">MFGetAttributesAsBlob</a> function.

This function deletes any attributes that were previously stored in <i>pAttributes</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 


---
UID: NF:mfapi.MFGetAttributesAsBlob
title: MFGetAttributesAsBlob function (mfapi.h)

description: Converts the contents of an attribute store to a byte array.
old-location: mf\mfgetattributesasblob.htm
tech.root: medfound
ms.assetid: 1a3bd860-1022-481f-8615-5a73c16dd77b

ms.date: 12/05/2018
ms.keywords: 1a3bd860-1022-481f-8615-5a73c16dd77b, MFGetAttributesAsBlob, MFGetAttributesAsBlob function [Media Foundation], mf.mfgetattributesasblob, mfapi/MFGetAttributesAsBlob
ms.topic: function
f1_keywords: 
 - "mfapi/MFGetAttributesAsBlob"
dev_langs:
 - c++
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
 - MFGetAttributesAsBlob
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFGetAttributesAsBlob function


## -description



Converts the contents of an attribute store to a byte array.




## -parameters




### -param pAttributes [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of the attribute store.


### -param pBuf [out]

Pointer to an array that receives the attribute data.


### -param cbBufSize [in]

Size of the <i>pBuf</i> array, in bytes. To get the required size of the buffer, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblobsize">MFGetAttributesAsBlobSize</a>.


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
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer given in <i>pBuf</i> is too small.

</td>
</tr>
</table>
 




## -remarks



The function skips any attributes with <b>IUnknown</b> pointer values (MF_ATTRIBUTE_IUNKNOWN); they are not stored in the array.

To convert the byte array back into an attribute store, call <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob">MFInitAttributesFromBlob</a>.

To write an attribute store to a stream, call the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream">MFSerializeAttributesToStream</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
 

 


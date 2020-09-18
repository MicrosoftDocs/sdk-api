---
UID: NF:textstor.ITextStoreAnchor.RetrieveRequestedAttrs
title: ITextStoreAnchor::RetrieveRequestedAttrs (textstor.h)
description: ITextStoreAnchor::RetrieveRequestedAttrs method
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","RetrieveRequestedAttrs method","ITextStoreAnchor.RetrieveRequestedAttrs","ITextStoreAnchor::RetrieveRequestedAttrs","RetrieveRequestedAttrs","RetrieveRequestedAttrs method [Text Services Framework]","RetrieveRequestedAttrs method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::RetrieveRequestedAttrs","tsf.itextstoreanchor_retrieverequestedattrs"]
old-location: tsf\itextstoreanchor_retrieverequestedattrs.htm
tech.root: TSF
ms.assetid: 36847680-bcf2-4db5-a587-90518f60cf5b
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],RetrieveRequestedAttrs method, ITextStoreAnchor.RetrieveRequestedAttrs, ITextStoreAnchor::RetrieveRequestedAttrs, RetrieveRequestedAttrs, RetrieveRequestedAttrs method [Text Services Framework], RetrieveRequestedAttrs method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::RetrieveRequestedAttrs, tsf.itextstoreanchor_retrieverequestedattrs
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITextStoreAnchor::RetrieveRequestedAttrs
 - textstor/ITextStoreAnchor::RetrieveRequestedAttrs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.RetrieveRequestedAttrs
---

# ITextStoreAnchor::RetrieveRequestedAttrs


## -description

Returns the attributes obtained by the RequestAttrsAtPosition, RequestAttrsTransitioningAtPosition, or RequestSupportedAttrs methods.

## -parameters

### -param ulCount [in]

Specifies the number of supported attributes to obtain.

### -param paAttrVals [out]

Pointer to the <a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a> structure that receives the supported attributes. The members of this structure depend upon the <i>dwFlags</i> parameter of the calling method.

### -param pcFetched [out]

Receives the number of supported attributes.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestattrsatposition">ITextStoreAnchor::RequestAttrsAtPosition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestattrstransitioningatposition">ITextStoreAnchor::RequestAttrsTransitioningAtPosition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-requestsupportedattrs">ITextStoreAnchor::RequestSupportedAttrs
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL
      </a>
---
UID: NF:textstor.ITextStoreACP2.RetrieveRequestedAttrs
title: ITextStoreACP2::RetrieveRequestedAttrs (textstor.h)
description: Gets the attributes returned by a call to an attribute request method. (ITextStoreACP2.RetrieveRequestedAttrs)
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","RetrieveRequestedAttrs method","ITextStoreACP2.RetrieveRequestedAttrs","ITextStoreACP2::RetrieveRequestedAttrs","RetrieveRequestedAttrs","RetrieveRequestedAttrs method [Text Services Framework]","RetrieveRequestedAttrs method [Text Services Framework]","ITextStoreACP2 interface","textstor/ITextStoreACP2::RetrieveRequestedAttrs","tsf.itextstoreacp2_retrieverequestedattrs"]
old-location: tsf\itextstoreacp2_retrieverequestedattrs.htm
tech.root: TSF
ms.assetid: fff22304-626e-4ae6-ac8c-f4a62ee823c2
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],RetrieveRequestedAttrs method, ITextStoreACP2.RetrieveRequestedAttrs, ITextStoreACP2::RetrieveRequestedAttrs, RetrieveRequestedAttrs, RetrieveRequestedAttrs method [Text Services Framework], RetrieveRequestedAttrs method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::RetrieveRequestedAttrs, tsf.itextstoreacp2_retrieverequestedattrs
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextStoreACP2::RetrieveRequestedAttrs
 - textstor/ITextStoreACP2::RetrieveRequestedAttrs
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
 - ITextStoreACP2.RetrieveRequestedAttrs
---

# ITextStoreACP2::RetrieveRequestedAttrs


## -description

Gets the attributes returned by a call to an attribute request method.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-requestattrsatposition">RequestAttrsAtPosition</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-requestattrstransitioningatposition">RequestAttrsTransitioningAtPosition</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-requestsupportedattrs">RequestSupportedAttrs</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a>

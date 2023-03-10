---
UID: NF:textstor.ITextStoreACP2.RequestSupportedAttrs
title: ITextStoreACP2::RequestSupportedAttrs (textstor.h)
description: Get the attributes that are supported in the document. (ITextStoreACP2.RequestSupportedAttrs)
helpviewer_keywords: ["ITextStoreACP2 interface [Text Services Framework]","RequestSupportedAttrs method","ITextStoreACP2.RequestSupportedAttrs","ITextStoreACP2::RequestSupportedAttrs","RequestSupportedAttrs","RequestSupportedAttrs method [Text Services Framework]","RequestSupportedAttrs method [Text Services Framework]","ITextStoreACP2 interface","textstor/ITextStoreACP2::RequestSupportedAttrs","tsf.itextstoreacp2_requestsupportedattrs"]
old-location: tsf\itextstoreacp2_requestsupportedattrs.htm
tech.root: TSF
ms.assetid: ce26c2ec-f808-4f59-bc54-b3681b97ad89
ms.date: 12/05/2018
ms.keywords: ITextStoreACP2 interface [Text Services Framework],RequestSupportedAttrs method, ITextStoreACP2.RequestSupportedAttrs, ITextStoreACP2::RequestSupportedAttrs, RequestSupportedAttrs, RequestSupportedAttrs method [Text Services Framework], RequestSupportedAttrs method [Text Services Framework],ITextStoreACP2 interface, textstor/ITextStoreACP2::RequestSupportedAttrs, tsf.itextstoreacp2_requestsupportedattrs
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
 - ITextStoreACP2::RequestSupportedAttrs
 - textstor/ITextStoreACP2::RequestSupportedAttrs
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
 - ITextStoreACP2.RequestSupportedAttrs
---

# ITextStoreACP2::RequestSupportedAttrs


## -description

Get the attributes that are supported in the document.

## -parameters

### -param dwFlags [in]

Specifies whether a subsequent call to the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp2-retrieverequestedattrs">RetrieveRequestedAttrs</a> method will contain the supported attributes. If the <b>TS_ATTR_FIND_WANT_VALUE</b> flag is specified, the default attribute values will be those in the <a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a> structure after the subsequent call to <b>RetrieveRequestedAttrs</b>. If any other flag is specified for this parameter, the method only verifies that the attribute is supported and that the <b>varValue</b> member of the <b>TS_ATTRVAL</b> structure is set to <b>VT_EMPTY</b>.

### -param cFilterAttrs [in]

Specifies the number of supported attributes to obtain.

### -param paFilterAttrs [in]

Pointer to the <a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> data type that specifies the attribute to verify. The method returns only the attributes specified by <b>TS_ATTRID</b>, even though other attributes can be supported.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate sufficient memory to complete the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a>

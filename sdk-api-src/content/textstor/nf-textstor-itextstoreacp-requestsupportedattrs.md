---
UID: NF:textstor.ITextStoreACP.RequestSupportedAttrs
title: ITextStoreACP::RequestSupportedAttrs (textstor.h)
description: Get the attributes that are supported in the document. (ITextStoreACP.RequestSupportedAttrs)
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","RequestSupportedAttrs method","ITextStoreACP.RequestSupportedAttrs","ITextStoreACP::RequestSupportedAttrs","RequestSupportedAttrs","RequestSupportedAttrs method [Text Services Framework]","RequestSupportedAttrs method [Text Services Framework]","ITextStoreACP interface","_tsf_itextstoreacp_requestsupportedattrs_ref","textstor/ITextStoreACP::RequestSupportedAttrs","tsf.itextstoreacp_requestsupportedattrs"]
old-location: tsf\itextstoreacp_requestsupportedattrs.htm
tech.root: TSF
ms.assetid: 243cd002-c882-4ce9-b528-1a2229c46f4a
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],RequestSupportedAttrs method, ITextStoreACP.RequestSupportedAttrs, ITextStoreACP::RequestSupportedAttrs, RequestSupportedAttrs, RequestSupportedAttrs method [Text Services Framework], RequestSupportedAttrs method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_requestsupportedattrs_ref, textstor/ITextStoreACP::RequestSupportedAttrs, tsf.itextstoreacp_requestsupportedattrs
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITextStoreACP::RequestSupportedAttrs
 - textstor/ITextStoreACP::RequestSupportedAttrs
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
 - ITextStoreACP.RequestSupportedAttrs
---

# ITextStoreACP::RequestSupportedAttrs


## -description

Get the attributes that are supported in the document.

## -parameters

### -param dwFlags [in]

Specifies whether a subsequent call to the <a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-retrieverequestedattrs">ITextStoreAnchor::RetrieveRequestedAttrs</a> method will contain the supported attributes. If the TS_ATTR_FIND_WANT_VALUE flag is specified, the default attribute values will be those in the <a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a> structure after the subsequent call to <b>ITextStoreAnchor::RetrieveRequestedAttrs</b>. If any other flag is specified for this parameter, the method only verifies that the attribute is supported and that the <b>varValue</b> member of the <b>TS_ATTRVAL</b> structure is set to VT_EMPTY.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-retrieverequestedattrs">ITextStoreACP::RetrieveRequestededAttrs
      </a>



<a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL
      </a>

---
UID: NF:textstor.ITextStoreAnchor.RequestSupportedAttrs
title: ITextStoreAnchor::RequestSupportedAttrs (textstor.h)
description: ITextStoreAnchor::RequestSupportedAttrs method
helpviewer_keywords: ["ITextStoreAnchor interface [Text Services Framework]","RequestSupportedAttrs method","ITextStoreAnchor.RequestSupportedAttrs","ITextStoreAnchor::RequestSupportedAttrs","RequestSupportedAttrs","RequestSupportedAttrs method [Text Services Framework]","RequestSupportedAttrs method [Text Services Framework]","ITextStoreAnchor interface","textstor/ITextStoreAnchor::RequestSupportedAttrs","tsf.itextstoreanchor_requestsupportedattrs"]
old-location: tsf\itextstoreanchor_requestsupportedattrs.htm
tech.root: TSF
ms.assetid: ab81d79d-e991-4c2d-9fb7-95393e002828
ms.date: 12/05/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],RequestSupportedAttrs method, ITextStoreAnchor.RequestSupportedAttrs, ITextStoreAnchor::RequestSupportedAttrs, RequestSupportedAttrs, RequestSupportedAttrs method [Text Services Framework], RequestSupportedAttrs method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::RequestSupportedAttrs, tsf.itextstoreanchor_requestsupportedattrs
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
 - ITextStoreAnchor::RequestSupportedAttrs
 - textstor/ITextStoreAnchor::RequestSupportedAttrs
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
 - ITextStoreAnchor.RequestSupportedAttrs
---

# ITextStoreAnchor::RequestSupportedAttrs


## -description

Obtains the supported attributes of a text stream.

## -parameters

### -param dwFlags [in]

Specifies whether a subsequent call to the <b>ITextStoreAnchor::RetrieveRequestedAttrs</b> method will contain the supported attributes. If the TS_ATTR_FIND_WANT_VALUE flag is specified, the default attribute values will be those in the <a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL</a> structure after the subsequent call to <b>ITextStoreAnchor::RetrieveRequestedAttrs</b>. If any other flag is specified for this parameter, the method only verifies that the attribute is supported and that the <b>varValue</b> member of the <b>TS_ATTRVAL</b> structure is set to VT_EMPTY.

### -param cFilterAttrs [in]

Specifies the number of supported attributes to obtain.

### -param paFilterAttrs [in]

Pointer to the <a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID</a> data type that specifies the attribute to verify. The method returns only the attributes specified by <b>TS_ATTRID</b>, even though other attributes might be supported.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchor-retrieverequestedattrs">ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="/windows/desktop/TSF/ts-attrid">TS_ATTRID
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL
      </a>
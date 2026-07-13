---
UID: NF:textstor.ITextStoreACP.RetrieveRequestedAttrs
title: ITextStoreACP::RetrieveRequestedAttrs (textstor.h)
description: Gets the attributes returned by a call to an attribute request method. (ITextStoreACP.RetrieveRequestedAttrs)
helpviewer_keywords: ["ITextStoreACP interface [Text Services Framework]","RetrieveRequestedAttrs method","ITextStoreACP.RetrieveRequestedAttrs","ITextStoreACP::RetrieveRequestedAttrs","RetrieveRequestedAttrs","RetrieveRequestedAttrs method [Text Services Framework]","RetrieveRequestedAttrs method [Text Services Framework]","ITextStoreACP interface","_tsf_itextstoreacp_retrieverequestedattrs_ref","textstor/ITextStoreACP::RetrieveRequestedAttrs","tsf.itextstoreacp_retrieverequestedattrs"]
old-location: tsf\itextstoreacp_retrieverequestedattrs.htm
tech.root: TSF
ms.assetid: 6cd34ca5-6561-4161-beac-98248f0415f6
ms.date: 12/05/2018
ms.keywords: ITextStoreACP interface [Text Services Framework],RetrieveRequestedAttrs method, ITextStoreACP.RetrieveRequestedAttrs, ITextStoreACP::RetrieveRequestedAttrs, RetrieveRequestedAttrs, RetrieveRequestedAttrs method [Text Services Framework], RetrieveRequestedAttrs method [Text Services Framework],ITextStoreACP interface, _tsf_itextstoreacp_retrieverequestedattrs_ref, textstor/ITextStoreACP::RetrieveRequestedAttrs, tsf.itextstoreacp_retrieverequestedattrs
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
 - ITextStoreACP::RetrieveRequestedAttrs
 - textstor/ITextStoreACP::RetrieveRequestedAttrs
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
 - ITextStoreACP.RetrieveRequestedAttrs
---

# ITextStoreACP::RetrieveRequestedAttrs


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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP</a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestattrsatposition">ITextStoreACP::RequestAttrsAtPosition
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestsupportedattrs">ITextStoreACP::RequestSupportedAttrs
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_attrval">TS_ATTRVAL
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-requestattrstransitioningatposition">TextStoreACP::RequestAttrsTransitioningAtPosition
      </a>

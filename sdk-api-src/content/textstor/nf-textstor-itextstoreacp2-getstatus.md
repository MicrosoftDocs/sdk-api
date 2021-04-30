---
UID: NF:textstor.ITextStoreACP2.GetStatus
title: ITextStoreACP2::GetStatus (textstor.h)
description: Gets the document status. The document status is returned through the TS_STATUS structure.
helpviewer_keywords: ["GetStatus","GetStatus method [Text Services Framework]","GetStatus method [Text Services Framework]","ITextStoreACP2 interface","ITextStoreACP2 interface [Text Services Framework]","GetStatus method","ITextStoreACP2.GetStatus","ITextStoreACP2::GetStatus","textstor/ITextStoreACP2::GetStatus","tsf.itextstoreacp2_getstatus"]
old-location: tsf\itextstoreacp2_getstatus.htm
tech.root: TSF
ms.assetid: 6b767f85-0a92-467c-b358-3629582f0d43
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetStatus method, ITextStoreACP2.GetStatus, ITextStoreACP2::GetStatus, textstor/ITextStoreACP2::GetStatus, tsf.itextstoreacp2_getstatus
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
 - ITextStoreACP2::GetStatus
 - textstor/ITextStoreACP2::GetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITextStoreACP2.GetStatus
---

# ITextStoreACP2::GetStatus


## -description

Gets the document status. The document status is returned through the <a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure.

## -parameters

### -param pdcs [out]

Receives the <a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure that contains the document status. Cannot be <b>NULL</b>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The pointer to the <a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> parameter is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp">ITextStoreACP
      </a>



<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacp2">ITextStoreACP2</a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getstatus">ITfContextOwner::GetStatus
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a>
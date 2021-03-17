---
UID: NF:textstor.ITextStoreAnchor.GetStatus
title: ITextStoreAnchor::GetStatus (textstor.h)
description: The ITextStoreAnchor::GetStatus method obtains the document status. The document status is returned through the TS_STATUS structure.
helpviewer_keywords: ["GetStatus","GetStatus method [Text Services Framework]","GetStatus method [Text Services Framework]","ITextStoreAnchor interface","ITextStoreAnchor interface [Text Services Framework]","GetStatus method","ITextStoreAnchor.GetStatus","ITextStoreAnchor::GetStatus","textstor/ITextStoreAnchor::GetStatus","tsf.itextstoreanchor_getstatus"]
old-location: tsf\itextstoreanchor_getstatus.htm
tech.root: TSF
ms.assetid: 61192268-5a5f-4caa-bdb8-799ee4aea24e
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITextStoreAnchor interface, ITextStoreAnchor interface [Text Services Framework],GetStatus method, ITextStoreAnchor.GetStatus, ITextStoreAnchor::GetStatus, textstor/ITextStoreAnchor::GetStatus, tsf.itextstoreanchor_getstatus
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
 - ITextStoreAnchor::GetStatus
 - textstor/ITextStoreAnchor::GetStatus
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
 - ITextStoreAnchor.GetStatus
---

# ITextStoreAnchor::GetStatus


## -description

The <b>ITextStoreAnchor::GetStatus</b> method obtains the document status. The document status is returned through the <a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure.

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
The pointer to the TS_STATUS parameter is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreanchor">ITextStoreAnchor
      </a>



<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreanchorsink-onstatuschange">ITextStoreAnchorSink::OnStatusChange
      </a>



<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getstatus">ITfContextOwner::GetStatus
      </a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS
      </a>
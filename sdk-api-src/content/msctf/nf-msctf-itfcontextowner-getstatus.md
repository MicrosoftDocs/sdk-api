---
UID: NF:msctf.ITfContextOwner.GetStatus
title: ITfContextOwner::GetStatus (msctf.h)
description: The ITfContextOwner::GetStatus method obtains the status of a document. The document status is returned through the TS_STATUS structure.
helpviewer_keywords: ["GetStatus","GetStatus method [Text Services Framework]","GetStatus method [Text Services Framework]","ITfContextOwner interface","ITfContextOwner interface [Text Services Framework]","GetStatus method","ITfContextOwner.GetStatus","ITfContextOwner::GetStatus","_tsf_itfcontextowner_getstatus_ref","msctf/ITfContextOwner::GetStatus","tsf.itfcontextowner_getstatus"]
old-location: tsf\itfcontextowner_getstatus.htm
tech.root: TSF
ms.assetid: ce30ec8a-48fe-4ec7-a7e1-2a0cf084097d
ms.date: 12/05/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITfContextOwner interface, ITfContextOwner interface [Text Services Framework],GetStatus method, ITfContextOwner.GetStatus, ITfContextOwner::GetStatus, _tsf_itfcontextowner_getstatus_ref, msctf/ITfContextOwner::GetStatus, tsf.itfcontextowner_getstatus
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msimtf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwner::GetStatus
 - msctf/ITfContextOwner::GetStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msimtf.dll
api_name:
 - ITfContextOwner.GetStatus
---

# ITfContextOwner::GetStatus


## -description

The <b>ITfContextOwner::GetStatus</b> method obtains the status of a document. The document status is returned through the <a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure.

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
</table>

## -see-also

<a href="/windows/desktop/api/textstor/nf-textstor-itextstoreacp-getstatus">ITextStoreACP::GetStatus
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextowner">ITfContextOwner</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS
      </a>
---
UID: NF:msctf.ITfContextOwnerServices.OnStatusChange
title: ITfContextOwnerServices::OnStatusChange (msctf.h)
description: The ITfContextOwnerServices::OnStatusChange method is called by the context owner when the dwDynamicFlags member of the TS_STATUS structure returned by the ITfContextOwner::GetStatus method changes.
helpviewer_keywords: ["ITfContextOwnerServices interface [Text Services Framework]","OnStatusChange method","ITfContextOwnerServices.OnStatusChange","ITfContextOwnerServices::OnStatusChange","OnStatusChange","OnStatusChange method [Text Services Framework]","OnStatusChange method [Text Services Framework]","ITfContextOwnerServices interface","_tsf_itfcontextownerservices_onstatuschange_ref","msctf/ITfContextOwnerServices::OnStatusChange","tsf.itfcontextownerservices_onstatuschange"]
old-location: tsf\itfcontextownerservices_onstatuschange.htm
tech.root: TSF
ms.assetid: da450910-d592-49c0-8df7-bc2f4037c4d2
ms.date: 12/05/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],OnStatusChange method, ITfContextOwnerServices.OnStatusChange, ITfContextOwnerServices::OnStatusChange, OnStatusChange, OnStatusChange method [Text Services Framework], OnStatusChange method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_onstatuschange_ref, msctf/ITfContextOwnerServices::OnStatusChange, tsf.itfcontextownerservices_onstatuschange
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfContextOwnerServices::OnStatusChange
 - msctf/ITfContextOwnerServices::OnStatusChange
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
 - ITfContextOwnerServices.OnStatusChange
---

# ITfContextOwnerServices::OnStatusChange


## -description

The <b>ITfContextOwnerServices::OnStatusChange</b> method is called by the context owner when the <b>dwDynamicFlags</b> member of the <a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure returned by the <a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getstatus">ITfContextOwner::GetStatus</a> method changes.

## -parameters

### -param dwFlags [in]

Specifies the dynamic status flag.

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

<a href="/windows/desktop/api/msctf/nf-msctf-itfcontextowner-getstatus">ITfContextOwner::GetStatus
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfcontextownerservices">ITfContextOwnerServices</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS
      </a>
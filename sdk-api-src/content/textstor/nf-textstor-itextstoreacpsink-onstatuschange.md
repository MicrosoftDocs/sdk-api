---
UID: NF:textstor.ITextStoreACPSink.OnStatusChange
title: ITextStoreACPSink::OnStatusChange (textstor.h)
description: ITextStoreACPSink::OnStatusChange method
helpviewer_keywords: ["ITextStoreACPSink interface [Text Services Framework]","OnStatusChange method","ITextStoreACPSink.OnStatusChange","ITextStoreACPSink::OnStatusChange","OnStatusChange","OnStatusChange method [Text Services Framework]","OnStatusChange method [Text Services Framework]","ITextStoreACPSink interface","_tsf_itextstoreacpsink_onstatuschange_ref","textstor/ITextStoreACPSink::OnStatusChange","tsf.itextstoreacpsink_onstatuschange"]
old-location: tsf\itextstoreacpsink_onstatuschange.htm
tech.root: TSF
ms.assetid: 44ecc116-e6f3-48dd-9bff-16d3c1e4cc97
ms.date: 12/05/2018
ms.keywords: ITextStoreACPSink interface [Text Services Framework],OnStatusChange method, ITextStoreACPSink.OnStatusChange, ITextStoreACPSink::OnStatusChange, OnStatusChange, OnStatusChange method [Text Services Framework], OnStatusChange method [Text Services Framework],ITextStoreACPSink interface, _tsf_itextstoreacpsink_onstatuschange_ref, textstor/ITextStoreACPSink::OnStatusChange, tsf.itextstoreacpsink_onstatuschange
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
 - ITextStoreACPSink::OnStatusChange
 - textstor/ITextStoreACPSink::OnStatusChange
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
 - ITextStoreACPSink.OnStatusChange
---

# ITextStoreACPSink::OnStatusChange


## -description

Called when the status of the document changes.

## -parameters

### -param dwFlags [in]

Contains a value that specifies the new status. For more information about possible values, see the <b>dwDynamicFlags</b> member of the <a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS</a> structure.

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

<a href="/windows/desktop/api/textstor/nn-textstor-itextstoreacpsink">ITextStoreACPSink</a>



<a href="/windows/desktop/api/textstor/ns-textstor-ts_status">TS_STATUS
      </a>
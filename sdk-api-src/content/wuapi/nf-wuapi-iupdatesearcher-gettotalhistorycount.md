---
UID: NF:wuapi.IUpdateSearcher.GetTotalHistoryCount
title: IUpdateSearcher::GetTotalHistoryCount (wuapi.h)
description: Returns the number of update events on the computer.
helpviewer_keywords: ["GetTotalHistoryCount","GetTotalHistoryCount method [Windows Update Agent]","GetTotalHistoryCount method [Windows Update Agent]","IUpdateSearcher interface","IUpdateSearcher interface [Windows Update Agent]","GetTotalHistoryCount method","IUpdateSearcher.GetTotalHistoryCount","IUpdateSearcher::GetTotalHistoryCount","wua.iupdatesearchergettotalhistorycount","wuapi/IUpdateSearcher::GetTotalHistoryCount"]
old-location: wua\iupdatesearchergettotalhistorycount.htm
tech.root: wua
ms.assetid: 895f60c2-c106-4088-9a4f-7c1d159d8a9b
ms.date: 12/05/2018
ms.keywords: GetTotalHistoryCount, GetTotalHistoryCount method [Windows Update Agent], GetTotalHistoryCount method [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],GetTotalHistoryCount method, IUpdateSearcher.GetTotalHistoryCount, IUpdateSearcher::GetTotalHistoryCount, wua.iupdatesearchergettotalhistorycount, wuapi/IUpdateSearcher::GetTotalHistoryCount
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateSearcher::GetTotalHistoryCount
 - wuapi/IUpdateSearcher::GetTotalHistoryCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher.GetTotalHistoryCount
---

# IUpdateSearcher::GetTotalHistoryCount


## -description

Returns the number of update events on the computer.

## -parameters

### -param retval [out]

The number of update events on the computer.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>
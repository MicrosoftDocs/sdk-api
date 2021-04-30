---
UID: NF:winsync.ISyncKnowledge2.GetStatistics
title: ISyncKnowledge2::GetStatistics (winsync.h)
description: Gets the specified statistic data that is contained in this object.
helpviewer_keywords: ["GetStatistics","GetStatistics method [Windows Sync]","GetStatistics method [Windows Sync]","ISyncKnowledge2 interface","ISyncKnowledge2 interface [Windows Sync]","GetStatistics method","ISyncKnowledge2.GetStatistics","ISyncKnowledge2::GetStatistics","winsync.isyncknowledge2_getstatistics","winsync/ISyncKnowledge2::GetStatistics"]
old-location: winsync\isyncknowledge2_getstatistics.htm
tech.root: winsync
ms.assetid: a7dea268-87d7-4e6d-9618-089036d52699
ms.date: 12/05/2018
ms.keywords: GetStatistics, GetStatistics method [Windows Sync], GetStatistics method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],GetStatistics method, ISyncKnowledge2.GetStatistics, ISyncKnowledge2::GetStatistics, winsync.isyncknowledge2_getstatistics, winsync/ISyncKnowledge2::GetStatistics
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncKnowledge2::GetStatistics
 - winsync/ISyncKnowledge2::GetStatistics
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncKnowledge2.GetStatistics
---

# ISyncKnowledge2::GetStatistics


## -description

Gets the specified statistic data that is contained in this object.

## -parameters

### -param which [in]

Specifies which statistic to retrieve.

### -param pValue [out]

The specified statistic data.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>which</i> is not a member of the <b>SYNC_STATISTICS</b> enumeration.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge">ISyncKnowledge Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncknowledge2">ISyncKnowledge2 Interface</a>



<a href="/windows/win32/api/winsync/ne-winsync-sync_statistics">SYNC_STATISTICS Enumeration</a>
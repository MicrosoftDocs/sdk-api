---
UID: NF:winsync.ISyncChangeBatchAdvanced.GetFilterInfo
title: ISyncChangeBatchAdvanced::GetFilterInfo (winsync.h)
description: Gets the ISyncFilterInfo that was specified when the change batch was created.
helpviewer_keywords: ["GetFilterInfo","GetFilterInfo method [Windows Sync]","GetFilterInfo method [Windows Sync]","ISyncChangeBatchAdvanced interface","ISyncChangeBatchAdvanced interface [Windows Sync]","GetFilterInfo method","ISyncChangeBatchAdvanced.GetFilterInfo","ISyncChangeBatchAdvanced::GetFilterInfo","winsync.isyncchangebatchadvanced_getfilterinfo","winsync/ISyncChangeBatchAdvanced::GetFilterInfo"]
old-location: winsync\isyncchangebatchadvanced_getfilterinfo.htm
tech.root: winsync
ms.assetid: f630f806-cc5a-408e-bd84-49555ebb41c1
ms.date: 12/05/2018
ms.keywords: GetFilterInfo, GetFilterInfo method [Windows Sync], GetFilterInfo method [Windows Sync],ISyncChangeBatchAdvanced interface, ISyncChangeBatchAdvanced interface [Windows Sync],GetFilterInfo method, ISyncChangeBatchAdvanced.GetFilterInfo, ISyncChangeBatchAdvanced::GetFilterInfo, winsync.isyncchangebatchadvanced_getfilterinfo, winsync/ISyncChangeBatchAdvanced::GetFilterInfo
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
 - ISyncChangeBatchAdvanced::GetFilterInfo
 - winsync/ISyncChangeBatchAdvanced::GetFilterInfo
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
 - ISyncChangeBatchAdvanced.GetFilterInfo
---

# ISyncChangeBatchAdvanced::GetFilterInfo


## -description

Gets the <a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo</a> that was specified when the change batch was created.

## -parameters

### -param ppFilterInfo [out]

Returns the <b>ISyncFilterInfo</b> that was specified when the change batch was created. <b>NULL</b> indicates that no filter was specified when the change batch was created.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No filter was specified when the change batch was created. In this situation, <b>NULL</b> is returned in <i>ppFilterInfo</i>.

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

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatchadvanced">ISyncChangeBatchAdvanced Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncfilterinfo">ISyncFilterInfo Interface</a>
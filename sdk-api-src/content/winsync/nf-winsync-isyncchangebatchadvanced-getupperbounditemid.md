---
UID: NF:winsync.ISyncChangeBatchAdvanced.GetUpperBoundItemId
title: ISyncChangeBatchAdvanced::GetUpperBoundItemId
author: windows-sdk-content
description: Gets the highest item ID that is represented in the knowledge of any group in the change batch.
old-location: winsync\isyncchangebatchadvanced_getupperbounditemid.htm
old-project: winsync
ms.assetid: 4aa472b1-7dfb-4159-8f50-cc8e5de34dd3
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetUpperBoundItemId, GetUpperBoundItemId method [Windows Sync], GetUpperBoundItemId method [Windows Sync],ISyncChangeBatchAdvanced interface, ISyncChangeBatchAdvanced interface [Windows Sync],GetUpperBoundItemId method, ISyncChangeBatchAdvanced.GetUpperBoundItemId, ISyncChangeBatchAdvanced::GetUpperBoundItemId, winsync.isyncchangebatchadvanced_getupperbounditemid, winsync/ISyncChangeBatchAdvanced::GetUpperBoundItemId
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeBatchAdvanced.GetUpperBoundItemId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchAdvanced::GetUpperBoundItemId


## -description


Gets the highest item ID that is represented in the knowledge of any group in the change batch.


## -parameters




### -param pbItemId [in, out]

Returns the highest item ID that is represented in the knowledge of any group in the change batch.


### -param pcbIdSize [in, out]

Specifies the number of bytes in <i>pbItemId</i>. Returns the number of bytes that are necessary to retrieve the ID when <i>pbItemId</i> is too small, or returns the number of bytes written.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_MORE_DATA)</b></dt>
</dl>
</td>
<td width="60%">
When <i>pbItemId</i> is too small. In this situation, the required number of bytes is returned in <i>pcbIdSize</i>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b78bc885-ed4e-4c83-ad1b-043c5b226337">ISyncChangeBatchAdvanced Interface</a>
 

 


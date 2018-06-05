---
UID: NF:winsync.ISyncChangeBatchAdvanced.GetFilterInfo
title: ISyncChangeBatchAdvanced::GetFilterInfo
author: windows-sdk-content
description: Gets the ISyncFilterInfo that was specified when the change batch was created.
old-location: winsync\isyncchangebatchadvanced_getfilterinfo.htm
old-project: winsync
ms.assetid: f630f806-cc5a-408e-bd84-49555ebb41c1
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetFilterInfo, GetFilterInfo method [Windows Sync], GetFilterInfo method [Windows Sync],ISyncChangeBatchAdvanced interface, ISyncChangeBatchAdvanced interface [Windows Sync],GetFilterInfo method, ISyncChangeBatchAdvanced.GetFilterInfo, ISyncChangeBatchAdvanced::GetFilterInfo, winsync.isyncchangebatchadvanced_getfilterinfo, winsync/ISyncChangeBatchAdvanced::GetFilterInfo
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChangeBatchAdvanced.GetFilterInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchAdvanced::GetFilterInfo


## -description


Gets the <a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo</a> that was specified when the change batch was created.


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




<a href="https://msdn.microsoft.com/b78bc885-ed4e-4c83-ad1b-043c5b226337">ISyncChangeBatchAdvanced Interface</a>



<a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo Interface</a>
 

 


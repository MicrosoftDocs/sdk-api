---
UID: NF:winsync.ISyncKnowledge2.GetStatistics
title: ISyncKnowledge2::GetStatistics
author: windows-sdk-content
description: Gets the specified statistic data that is contained in this object.
old-location: winsync\isyncknowledge2_getstatistics.htm
old-project: winsync
ms.assetid: a7dea268-87d7-4e6d-9618-089036d52699
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetStatistics, GetStatistics method [Windows Sync], GetStatistics method [Windows Sync],ISyncKnowledge2 interface, ISyncKnowledge2 interface [Windows Sync],GetStatistics method, ISyncKnowledge2.GetStatistics, ISyncKnowledge2::GetStatistics, winsync.isyncknowledge2_getstatistics, winsync/ISyncKnowledge2::GetStatistics
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
 - ISyncKnowledge2.GetStatistics
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>



<a href="https://msdn.microsoft.com/1acbae32-8fa6-4c1e-95f6-30aca483c966">ISyncKnowledge2 Interface</a>



<a href="https://msdn.microsoft.com/8a978578-0169-4784-bdcf-ff41f0a09f7a">SYNC_STATISTICS Enumeration</a>
 

 


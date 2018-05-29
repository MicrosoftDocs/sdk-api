---
UID: NF:winsync.ISyncChangeBatchBase.GetSourceForgottenKnowledge
title: ISyncChangeBatchBase::GetSourceForgottenKnowledge
author: windows-sdk-content
description: Gets the forgotten knowledge of the source replica.
old-location: winsync\isyncchangebatchbase_getsourceforgottenknowledge.htm
old-project: winsync
ms.assetid: 309b2c83-4480-421c-ae90-9cbe7ac11055
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetSourceForgottenKnowledge, GetSourceForgottenKnowledge method [Windows Sync], GetSourceForgottenKnowledge method [Windows Sync],ISyncChangeBatchBase interface, ISyncChangeBatchBase interface [Windows Sync],GetSourceForgottenKnowledge method, ISyncChangeBatchBase.GetSourceForgottenKnowledge, ISyncChangeBatchBase::GetSourceForgottenKnowledge, winsync.isyncchangebatchbase_getsourceforgottenknowledge, winsync/ISyncChangeBatchBase::GetSourceForgottenKnowledge
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncChangeBatchBase.GetSourceForgottenKnowledge
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncChangeBatchBase::GetSourceForgottenKnowledge


## -description


Gets the forgotten knowledge of the source replica.


## -parameters




### -param ppSourceForgottenKnowledge [out]

Returns the forgotten knowledge of the source replica.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/14ca01a1-04eb-4282-adf0-e775d6ff0801">ISyncChangeBatchBase Interface</a>



<a href="https://msdn.microsoft.com/cfb08476-7b5d-4953-b723-5160330e57be">ISyncKnowledge Interface</a>
 

 


---
UID: NF:winsync.ISyncChangeBatchWithPrerequisite.GetLearnedForgottenKnowledge
title: ISyncChangeBatchWithPrerequisite::GetLearnedForgottenKnowledge
author: windows-sdk-content
description: Gets the forgotten knowledge that the destination replica learns when the destination provider applies all the changes in this change batch during recovery synchronization.
old-location: winsync\isyncchangebatchwithprerequisite_getlearnedforgottenknowledge.htm
tech.root: winsync
ms.assetid: 4e7a9f72-7d5e-4ef8-824a-d7623b71cfb5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetLearnedForgottenKnowledge, GetLearnedForgottenKnowledge method [Windows Sync], GetLearnedForgottenKnowledge method [Windows Sync],ISyncChangeBatchWithPrerequisite interface, ISyncChangeBatchWithPrerequisite interface [Windows Sync],GetLearnedForgottenKnowledge method, ISyncChangeBatchWithPrerequisite.GetLearnedForgottenKnowledge, ISyncChangeBatchWithPrerequisite::GetLearnedForgottenKnowledge, winsync.isyncchangebatchwithprerequisite_getlearnedforgottenknowledge, winsync/ISyncChangeBatchWithPrerequisite::GetLearnedForgottenKnowledge
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncChangeBatchWithPrerequisite.GetLearnedForgottenKnowledge
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncChangeBatchWithPrerequisite::GetLearnedForgottenKnowledge


## -description


Gets the forgotten knowledge that the destination replica learns when the destination provider applies all the changes in this change batch during recovery synchronization.


## -parameters




### -param ppLearnedForgottenKnowledge [out]

Returns the forgotten knowledge that the destination replica learns when the destination provider applies all the changes in this change batch during recovery synchronization.


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
<dt><b>SYNC_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The change batch object is not an <a href="https://msdn.microsoft.com/9086991d-03e3-4f2c-ad03-c1f554fe32ce">ISyncFullEnumerationChangeBatch</a> object.

</td>
</tr>
</table>
 




## -remarks



The knowledge returned in <i>ppLearnedForgottenKnowledge</i> is the source forgotten knowledge of the change batch projected onto the range contained in the change batch.




## -see-also




<a href="https://msdn.microsoft.com/93185921-8f41-4222-86d8-602d197c4b33">IForgottenKnowledge Interface</a>



<a href="https://msdn.microsoft.com/29d767cf-3261-4550-8b28-5d3950b8ded1">ISyncChangeBatchWithPrerequisite Interface</a>
 

 


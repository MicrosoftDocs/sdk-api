---
UID: NN:winsync.ISyncSessionState
title: ISyncSessionState (winsync.h)
author: windows-sdk-content
description: Represents information about the current synchronization session.
old-location: winsync\isyncsessionstate.htm
tech.root: winsync
ms.assetid: 9b03d5af-b5f5-49fa-a10e-9f9f3c1dab0e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncSessionState, ISyncSessionState interface [Windows Sync], ISyncSessionState interface [Windows Sync],described, winsync.isyncsessionstate, winsync/ISyncSessionState
ms.topic: interface
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
 - ISyncSessionState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncSessionState interface


## -description


Represents information about the current synchronization session.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncSessionState</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncSessionState</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncSessionState</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ba23805-cb1a-4178-a230-8091e3938fb6">GetForgottenKnowledgeRecoveryRangeEnd</a>
</td>
<td align="left" width="63%">
Gets the upper bound of the recovery range when the session is performing forgotten knowledge recovery.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6d6434a-d4cf-4b92-958c-5ff8022a9531">GetForgottenKnowledgeRecoveryRangeStart</a>
</td>
<td align="left" width="63%">
Gets the lower bound of the recovery range when the session is performing forgotten knowledge recovery.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88f7f8f7-468f-4d9d-9593-0d3f92cb458f">GetInfoForChangeApplication</a>
</td>
<td align="left" width="63%">
Retrieves stored data for a serialized change applier.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25ce0e21-99ce-4790-8f53-39466da9226f">IsCanceled</a>
</td>
<td align="left" width="63%">
Indicates whether the synchronization session has been canceled.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72c7947b-0eee-4b75-aff6-f208bebac3f2">LoadInfoFromChangeApplication</a>
</td>
<td align="left" width="63%">
Stores data for a serialized change applier.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a2983f9c-ed2d-47b4-bec7-b00dc4d75f3f">OnProgress</a>
</td>
<td align="left" width="63%">
Reports progress periodically during the synchronization session.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2de6bfb3-bde9-49ee-97eb-acc1671efd0d">SetForgottenKnowledgeRecoveryRange</a>
</td>
<td align="left" width="63%">
Sets the recovery range when the session is performing forgotten knowledge recovery.


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 


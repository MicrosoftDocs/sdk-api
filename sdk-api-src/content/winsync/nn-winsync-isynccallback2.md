---
UID: NN:winsync.ISyncCallback2
title: ISyncCallback2
author: windows-sdk-content
description: Represents additional application callbacks that are used to notify the application of synchronization events.
old-location: winsync\isynccallback2.htm
tech.root: winsync
ms.assetid: d2d690ba-8da2-4d53-a42c-14e4f010bc2d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISyncCallback2, ISyncCallback2 interface [Windows Sync], ISyncCallback2 interface [Windows Sync],described, winsync.isynccallback2, winsync/ISyncCallback2
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISyncCallback2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncCallback2 interface


## -description


Represents additional application callbacks that are used to notify the application of synchronization events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncCallback2</b> interface inherits from <a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback</a>. <b>ISyncCallback2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncCallback2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3397ca51-583b-4051-892b-68f505d85ccd">OnChangeApplied</a>
</td>
<td align="left" width="63%">
Occurs after a change is successfully applied.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69064507-414b-49be-91a5-3523160f3a01">OnChangeFailed</a>
</td>
<td align="left" width="63%">
Occurs after a change fails to apply.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4c2f7237-32ac-4f2d-bf6a-7959bc5d40d4">CONFLICT_RESOLUTION_POLICY Enumeration</a>



<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 


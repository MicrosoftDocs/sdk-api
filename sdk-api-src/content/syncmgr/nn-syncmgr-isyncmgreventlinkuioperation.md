---
UID: NN:syncmgr.ISyncMgrEventLinkUIOperation
title: ISyncMgrEventLinkUIOperation
author: windows-sdk-content
description: Provides a method that is called when event links are clicked in the sync results folder.
old-location: shell\ISyncMgrEventLinkUIOperation.htm
tech.root: shell
ms.assetid: 53ea9488-77e0-4eb2-86d3-88747ba44654
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: ISyncMgrEventLinkUIOperation, ISyncMgrEventLinkUIOperation interface [Windows Shell], ISyncMgrEventLinkUIOperation interface [Windows Shell],described, _shell_ISyncMgrEventLinkUIOperation, shell.ISyncMgrEventLinkUIOperation, syncmgr/ISyncMgrEventLinkUIOperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - Syncmgr.h
api_name:
 - ISyncMgrEventLinkUIOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrEventLinkUIOperation interface


## -description


Provides a method that is called when event links are clicked in the sync results folder.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrEventLinkUIOperation</b> interface inherits from <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a>. <b>ISyncMgrEventLinkUIOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrEventLinkUIOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f9c9fd9-54f9-423d-af91-6f569a7c8616">Init</a>
</td>
<td align="left" width="63%">
Enables Sync Center to provide the event to link to so <a href="https://msdn.microsoft.com/66dd853e-0fb0-4736-982a-e0183cb51842">ISyncMgrUIOperation::Run</a>  knows which event to operate upon.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/6fa4b0ac-3c75-4cda-b20d-582a3e18fb28">ISyncMgrUIOperation</a> interface, from which it inherits.

Sync Center calls <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">ISyncMgrHandler::GetObject</a>, specifying SYNCMGR_OBJECTID_EventLinkClick for the object ID.




---
UID: NN:cscobj.IOfflineFilesConnectionInfo
title: IOfflineFilesConnectionInfo
author: windows-sdk-content
description: Presents query and action capabilities associated with the online-offline transition behavior of Offline Files.
old-location: of\iofflinefilesconnectioninfo.htm
old-project: OfflineFiles
ms.assetid: 923c5657-67e7-498a-a46b-97d44368cf3b
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IOfflineFilesConnectionInfo, IOfflineFilesConnectionInfo interface [Offline Files], IOfflineFilesConnectionInfo interface [Offline Files],described, cscobj/IOfflineFilesConnectionInfo, of.iofflinefilesconnectioninfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesConnectionInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesConnectionInfo interface


## -description


Presents query and action capabilities associated with the online-offline transition behavior of Offline Files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesConnectionInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesConnectionInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesConnectionInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83b082b4-5845-44b7-9456-f00b357e345a">GetConnectState</a>
</td>
<td align="left" width="63%">
Determines whether an item is online or offline and, if offline, why.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42412f42-7a70-4110-88ec-a38b3df7d2da">SetConnectState</a>
</td>
<td align="left" width="63%">
Sets the connection state for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb32238d-c8f2-4228-8472-4a699b24c621">TransitionOffline</a>
</td>
<td align="left" width="63%">
Transitions an item offline if possible.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8cac664-598d-43fd-a77e-e8406c197afc">TransitionOnline</a>
</td>
<td align="left" width="63%">
Transitions an item online if possible.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 


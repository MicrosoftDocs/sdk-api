---
UID: NN:mmc.ISnapinHelp2
title: ISnapinHelp2
author: windows-sdk-content
description: Allows snap-ins to add HTML Help support.
old-location: mmc\isnapinhelp2.htm
tech.root: mmc
ms.assetid: 6e86a22b-03b0-4ca6-a4e2-96ea365dabdf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISnapinHelp2, ISnapinHelp2 interface [MMC], ISnapinHelp2 interface [MMC],described, _slate_isnapinhelp2, mmc.isnapinhelp2, mmc/ISnapinHelp2
ms.topic: interface
req.header: mmc.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinHelp2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISnapinHelp2 interface


## -description


The 
<b>ISnapinHelp2</b> interface is introduced in MMC 1.1.

The 
<b>ISnapinHelp2</b> interface allows snap-ins to add HTML Help support.<b>ISnapinHelp2</b> is a new version of the <b>ISnapinHelp</b> interface for MMC 1.1.

<b>ISnapinHelp2</b> is the same as <b>ISnapinHelp</b> with the addition of the following method:
<ul>
<li>
<a href="https://msdn.microsoft.com/ceed0d9f-e1bf-4692-aadf-e924095cdfc8">ISnapinHelp2::GetLinkedTopics</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinHelp2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISnapinHelp2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISnapinHelp2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a7157e34-6f38-4589-b85e-8aca2bcd6ee1">GetHelpTopic</a>
</td>
<td align="left" width="63%">
Merges the snap-in's HTML Help file into the MMC HTML Help file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ceed0d9f-e1bf-4692-aadf-e924095cdfc8">GetLinkedTopics</a>
</td>
<td align="left" width="63%">
Allows the snap-in to specify the names and locations of any HTML Help files that are linked to the snap-in's Help file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/87387cf5-ff5f-4816-8c96-97a7ae25df94">Adding HTML Help Support</a>
 

 


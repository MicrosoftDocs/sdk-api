---
UID: NN:mmc.IDisplayHelp
title: IDisplayHelp
author: windows-sdk-content
description: The IDisplayHelp interface is introduced in MMC version 1.1.
old-location: mmc\idisplayhelp.htm
tech.root: mmc
ms.assetid: 5f5b9a3b-d520-4e19-8cd7-efbb08bcfba2
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IDisplayHelp, IDisplayHelp interface [MMC], IDisplayHelp interface [MMC],described, _slate_idisplayhelp, mmc.idisplayhelp, mmc/IDisplayHelp
ms.prod: windows
ms.technology: windows-sdk
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IDisplayHelp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDisplayHelp interface


## -description


The 
<b>IDisplayHelp</b> interface is introduced in MMC version 1.1.

The 
<b>IDisplayHelp</b> interface enables a snap-in to display a specific HTML Help topic within the merged MMC HTML Help file. If the snap-in implemented 
<a href="https://msdn.microsoft.com/a7157e34-6f38-4589-b85e-8aca2bcd6ee1">ISnapinHelp2::GetHelpTopic</a>, MMC merges the snap-in's compiled HTML Help file (.chm) into the MMC HTML Help collection file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDisplayHelp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDisplayHelp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDisplayHelp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/184adc09-8b48-4a2e-bbd9-ec6bd9085c32">ShowTopic</a>
</td>
<td align="left" width="63%">
Displays the specified HTML Help topic in the merged MMC HTML Help file.

</td>
</tr>
</table> 


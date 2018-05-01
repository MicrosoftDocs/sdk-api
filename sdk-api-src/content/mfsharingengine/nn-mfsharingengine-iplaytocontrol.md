---
UID: NN:mfsharingengine.IPlayToControl
title: IPlayToControl
author: windows-driver-content
description: Enables the PlayToConnection object to connect to a media element.
old-location: mf\iplaytocontrol.htm
old-project: medfound
ms.assetid: 53355EEA-559B-4803-89F6-D454E15F9254
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IPlayToControl, IPlayToControl interface [Media Foundation], IPlayToControl interface [Media Foundation], described, mf.iplaytocontrol, mfsharingengine/IPlayToControl
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PLAYTO_SOURCE_CREATEFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfsharingengine.h
api_name:
-	IPlayToControl
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPlayToControl interface


## -description


Enables the <b>PlayToConnection</b> object to connect to a media element.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPlayToControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPlayToControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPlayToControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5252DC51-E1EF-4A61-A2BD-682F51DC219B">Connect</a>
</td>
<td align="left" width="63%">
Connects the media element to the media sharing engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59EA778D-25DA-4EEA-8601-F6D72486410B">Disconnect</a>
</td>
<td align="left" width="63%">
Disconnects the media element from the media sharing engine.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


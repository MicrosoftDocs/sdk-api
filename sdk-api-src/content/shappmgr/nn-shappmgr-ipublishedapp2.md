---
UID: NN:shappmgr.IPublishedApp2
title: IPublishedApp2
author: windows-sdk-content
description: Extends the IPublishedApp interface by providing an additional installation method.
old-location: shell\IPublishedApp2.htm
tech.root: shell
ms.assetid: 07d10120-7a91-4ed8-a0af-6ebac10622e3
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IPublishedApp2, IPublishedApp2 interface [Windows Shell], IPublishedApp2 interface [Windows Shell],described, _shell_IPublishedApp2, shappmgr/IPublishedApp2, shell.IPublishedApp2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - Shappmgr.h
api_name:
 - IPublishedApp2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPublishedApp2 interface


## -description


Extends the <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> interface by providing an additional installation method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPublishedApp2</b> interface inherits from <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a>. <b>IPublishedApp2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPublishedApp2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce2319d0-e4e8-49a8-9803-ef386c6969a9">Install2</a>
</td>
<td align="left" width="63%">
Installs an application published by an application publisher, while preventing multiple windows from being active on the same thread.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://msdn.microsoft.com/a5a44e74-494a-4c9b-8bf3-85c6093b2c0e">IPublishedApp</a> interface, from which it inherits.




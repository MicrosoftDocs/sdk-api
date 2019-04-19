---
UID: NN:mmc.ISnapinHelp
title: ISnapinHelp (mmc.h)
author: windows-sdk-content
description: Allows snap-ins to add HTML Help support.
old-location: mmc\isnapinhelp.htm
tech.root: mmc
ms.assetid: 237E52F7-5EB9-45DA-ACC3-391ED3BF7C5E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISnapinHelp, ISnapinHelp interface [MMC], ISnapinHelp interface [MMC],described, mmc.isnapinhelp, mmc/ISnapinHelp
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
req.idl: Mmc.idl
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
 - ISnapinHelp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISnapinHelp interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Allows snap-ins to add HTML Help support.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinHelp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISnapinHelp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISnapinHelp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/252403ef-6814-4ec0-bfef-ce5ca088bf41">GetHelpTopic</a>
</td>
<td align="left" width="63%">
Merges the snap-in's HTML Help file into the MMC HTML Help file.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/87387cf5-ff5f-4816-8c96-97a7ae25df94">Adding HTML Help Support</a>



<a href="https://msdn.microsoft.com/c95742a4-ae9b-40f3-8d88-c4955e5a3032">MMC 2.0 Interfaces and Methods</a>
 

 


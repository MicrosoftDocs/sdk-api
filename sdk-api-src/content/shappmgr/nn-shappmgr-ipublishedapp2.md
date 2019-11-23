---
UID: NN:shappmgr.IPublishedApp2
title: IPublishedApp2 (shappmgr.h)

description: Extends the IPublishedApp interface by providing an additional installation method.
old-location: shell\IPublishedApp2.htm
tech.root: shell
ms.assetid: 07d10120-7a91-4ed8-a0af-6ebac10622e3

ms.date: 12/05/2018
ms.keywords: IPublishedApp2, IPublishedApp2 interface [Windows Shell], IPublishedApp2 interface [Windows Shell],described, _shell_IPublishedApp2, shappmgr/IPublishedApp2, shell.IPublishedApp2
ms.topic: interface
f1_keywords: 
 - "shappmgr/IPublishedApp2"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPublishedApp2 interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> interface by providing an additional installation method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPublishedApp2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a>. <b>IPublishedApp2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nf-shappmgr-ipublishedapp2-install2">Install2</a>
</td>
<td align="left" width="63%">
Installs an application published by an application publisher, while preventing multiple windows from being active on the same thread.

</td>
</tr>
</table> 


## -remarks



This interface also provides the methods of the <a href="https://docs.microsoft.com/windows/desktop/api/shappmgr/nn-shappmgr-ipublishedapp">IPublishedApp</a> interface, from which it inherits.




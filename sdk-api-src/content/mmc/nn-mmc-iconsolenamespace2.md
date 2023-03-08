---
UID: NN:mmc.IConsoleNameSpace2
title: IConsoleNameSpace2 (mmc.h)
description: The IConsoleNameSpace2 interface is introduced in MMC 1.1.
helpviewer_keywords: ["IConsoleNameSpace","IConsoleNameSpace interface [MMC]","IConsoleNameSpace interface [MMC]","described","IConsoleNameSpace2","IConsoleNameSpace2 interface [MMC]","IConsoleNameSpace2 interface [MMC]","described","_slate_iconsolenamespace2","mmc.iconsolenamespace2","mmc/IConsoleNameSpace","mmc/IConsoleNameSpace2"]
old-location: mmc\iconsolenamespace2.htm
tech.root: mmc
ms.assetid: 894f99a6-2189-458d-a50f-497930d4a9dd
ms.date: 12/05/2018
ms.keywords: IConsoleNameSpace, IConsoleNameSpace interface [MMC], IConsoleNameSpace interface [MMC],described, IConsoleNameSpace2, IConsoleNameSpace2 interface [MMC], IConsoleNameSpace2 interface [MMC],described, _slate_iconsolenamespace2, mmc.iconsolenamespace2, mmc/IConsoleNameSpace, mmc/IConsoleNameSpace2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsoleNameSpace2
 - mmc/IConsoleNameSpace2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsoleNameSpace2
---

# IConsoleNameSpace2 interface


## -description

The 
<b>IConsoleNameSpace2</b> interface is introduced in MMC 1.1.

The 
<b>IConsoleNameSpace2</b> interface enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer. For example, a snap-in that features a domain object might enumerate individual groups or organizations within the domain.

<b>IConsoleNameSpace2</b> supersedes the <b>IConsoleNameSpace</b> interface for MMC 1.1. In addition to inheriting all of the methods of <b>IConsoleNameSpace</b>, 
<b>IConsoleNameSpace2</b> has the following methods:
<ul>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-expand">IConsoleNameSpace2::Expand</a>
</li>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-addextension">IConsoleNameSpace2::AddExtension</a>
</li>
</ul>The snap-in can query for a pointer to the 
<b>IConsoleNameSpace2</b> interface during a call to its 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-initialize">IComponentData::Initialize</a> method.

## -inheritance

The <b>IConsoleNameSpace2</b> interface inherits from <b>IConsoleNameSpace</b>. <b>IConsoleNameSpace2</b> also has these types of members:


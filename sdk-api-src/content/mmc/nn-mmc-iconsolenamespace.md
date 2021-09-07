---
UID: NN:mmc.IConsoleNameSpace
title: IConsoleNameSpace (mmc.h)
description: Enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer.
helpviewer_keywords: ["IConsoleNameSpace","IConsoleNameSpace interface [MMC]","IConsoleNameSpace interface [MMC]","described","mmc.iconsolenamespace","mmc/IConsoleNameSpace"]
old-location: mmc\iconsolenamespace.htm
tech.root: mmc
ms.assetid: 0E72A4DF-5A74-49DD-BD94-06860EFFE09A
ms.date: 12/05/2018
ms.keywords: IConsoleNameSpace, IConsoleNameSpace interface [MMC], IConsoleNameSpace interface [MMC],described, mmc.iconsolenamespace, mmc/IConsoleNameSpace
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsoleNameSpace
 - mmc/IConsoleNameSpace
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
 - IConsoleNameSpace
---

# IConsoleNameSpace interface


## -description

<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables snap-ins to enumerate dynamic subcontainers in the scope pane. The particular snap-in determines what qualifies as a subcontainer. For example, a snap-in that features a domain object might enumerate individual groups or organizations within the domain.

The snap-in can query for a pointer to the 
<b>IConsoleNameSpace</b> interface during a call to its 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-initialize">IComponentData::Initialize</a> method.

## -inheritance

The <b>IConsoleNameSpace</b> interface inherits from <b>IConsoleNameSpace</b>. <b>IConsoleNameSpace</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>



<a href="/previous-versions/windows/desktop/mmc/mmc-interfaces-and-methods">MMC 2.0 Interfaces and Methods</a>

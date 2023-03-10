---
UID: NN:mmc.IConsole2
title: IConsole2 (mmc.h)
description: The IConsole2 interface is introduced in MMC 1.1.
helpviewer_keywords: ["IConsole2","IConsole2 interface [MMC]","IConsole2 interface [MMC]","described","_slate_iconsole2","mmc.iconsole2","mmc/IConsole2"]
old-location: mmc\iconsole2.htm
tech.root: mmc
ms.assetid: 9a20d09d-219c-4bcb-95b3-67a44e41629e
ms.date: 12/05/2018
ms.keywords: IConsole2, IConsole2 interface [MMC], IConsole2 interface [MMC],described, _slate_iconsole2, mmc.iconsole2, mmc/IConsole2
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
 - IConsole2
 - mmc/IConsole2
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
 - IConsole2
---

# IConsole2 interface


## -description

The 
<b>IConsole2</b> interface is introduced in MMC 1.1.

The 
<b>IConsole2</b> interface enables communication with the console.

<b>IConsole2</b> is the same as <b>IConsole</b> with the addition of the following methods:
<ul>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole2-expand">IConsole2::Expand</a>
</li>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole2-istaskpadviewpreferred">IConsole2::IsTaskpadViewPreferred</a>
</li>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iconsole2-setstatustext">IConsole2::SetStatusText</a>
</li>
</ul>

## -inheritance

The <b>IConsole2</b> interface inherits from <a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>. <b>IConsole2</b> also has these types of members:


---
UID: NN:mmc.IDisplayHelp
title: IDisplayHelp (mmc.h)
description: The IDisplayHelp interface is introduced in MMC version 1.1.
helpviewer_keywords: ["IDisplayHelp","IDisplayHelp interface [MMC]","IDisplayHelp interface [MMC]","described","_slate_idisplayhelp","mmc.idisplayhelp","mmc/IDisplayHelp"]
old-location: mmc\idisplayhelp.htm
tech.root: mmc
ms.assetid: 5f5b9a3b-d520-4e19-8cd7-efbb08bcfba2
ms.date: 12/05/2018
ms.keywords: IDisplayHelp, IDisplayHelp interface [MMC], IDisplayHelp interface [MMC],described, _slate_idisplayhelp, mmc.idisplayhelp, mmc/IDisplayHelp
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
 - IDisplayHelp
 - mmc/IDisplayHelp
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
 - IDisplayHelp
---

# IDisplayHelp interface


## -description

The 
<b>IDisplayHelp</b> interface is introduced in MMC version 1.1.

The 
<b>IDisplayHelp</b> interface enables a snap-in to display a specific HTML Help topic within the merged MMC HTML Help file. If the snap-in implemented 
<a href="/previous-versions/windows/desktop/legacy/aa814944(v=vs.85)">ISnapinHelp2::GetHelpTopic</a>, MMC merges the snap-in's compiled HTML Help file (.chm) into the MMC HTML Help collection file.

## -inheritance

The <b>IDisplayHelp</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDisplayHelp</b> also has these types of members:


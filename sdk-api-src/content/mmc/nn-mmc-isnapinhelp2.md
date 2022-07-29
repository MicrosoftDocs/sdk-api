---
UID: NN:mmc.ISnapinHelp2
title: ISnapinHelp2 (mmc.h)
description: Allows snap-ins to add HTML Help support. (ISnapinHelp2)
helpviewer_keywords: ["ISnapinHelp2","ISnapinHelp2 interface [MMC]","ISnapinHelp2 interface [MMC]","described","_slate_isnapinhelp2","mmc.isnapinhelp2","mmc/ISnapinHelp2"]
old-location: mmc\isnapinhelp2.htm
tech.root: mmc
ms.assetid: 6e86a22b-03b0-4ca6-a4e2-96ea365dabdf
ms.date: 12/05/2018
ms.keywords: ISnapinHelp2, ISnapinHelp2 interface [MMC], ISnapinHelp2 interface [MMC],described, _slate_isnapinhelp2, mmc.isnapinhelp2, mmc/ISnapinHelp2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISnapinHelp2
 - mmc/ISnapinHelp2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - ISnapinHelp2
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
<a href="/windows/desktop/api/mmc/nf-mmc-isnapinhelp2-getlinkedtopics">ISnapinHelp2::GetLinkedTopics</a>
</li>
</ul>

## -inheritance

The <b>ISnapinHelp2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISnapinHelp2</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/mmc/adding-html-help-support">Adding HTML Help Support</a>

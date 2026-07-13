---
UID: NN:mmc.IComponent2
title: IComponent2 (mmc.h)
description: The IComponent2 interface, implemented by snap-ins, is introduced in MMC 2.0 and supersedes the IComponent interface.
helpviewer_keywords: ["IComponent2","IComponent2 interface [MMC]","IComponent2 interface [MMC]","described","_slate_icomponent2","mmc.icomponent2","mmc/IComponent2"]
old-location: mmc\icomponent2.htm
tech.root: mmc
ms.assetid: b9e67a37-c09d-46f3-896f-e75122256812
ms.date: 12/05/2018
ms.keywords: IComponent2, IComponent2 interface [MMC], IComponent2 interface [MMC],described, _slate_icomponent2, mmc.icomponent2, mmc/IComponent2
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
 - IComponent2
 - mmc/IComponent2
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
 - IComponent2
---

# IComponent2 interface


## -description

The 
<b>IComponent2</b> interface, implemented by snap-ins, is introduced in MMC 2.0 and supersedes the 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface.

Snap-ins written for MMC 2.0 and later should implement 
<b>IComponent2</b>, as the 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-getresultviewtype2">IComponent2::GetResultViewType2</a> and 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-restoreresultview">IComponent2::RestoreResultView</a> methods provide a way to precisely restoring a result view.

Additionally, the 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent2-querydispatch">IComponent2::QueryDispatch</a> method provides an IDispatch interface to the 
<a href="/previous-versions/windows/desktop/mmc/view-object">View</a> object for use with the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.

## -inheritance

The <b>IComponent2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IComponent2</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/mmc/restoring-result-views">Restoring Result Views</a>

---
UID: NF:wuapi.IUpdateSearcher.put_CanAutomaticallyUpgradeService
title: IUpdateSearcher::put_CanAutomaticallyUpgradeService (wuapi.h)
description: Gets and sets a Boolean value that indicates whether future calls to the BeginSearch and Search methods result in an automatic upgrade to Windows Update Agent (WUA). (Put)
helpviewer_keywords: ["CanAutomaticallyUpgradeService property [Windows Update Agent]","CanAutomaticallyUpgradeService property [Windows Update Agent]","IUpdateSearcher interface","IUpdateSearcher interface [Windows Update Agent]","CanAutomaticallyUpgradeService property","IUpdateSearcher.CanAutomaticallyUpgradeService","IUpdateSearcher.put_CanAutomaticallyUpgradeService","IUpdateSearcher::CanAutomaticallyUpgradeService","IUpdateSearcher::get_CanAutomaticallyUpgradeService","IUpdateSearcher::put_CanAutomaticallyUpgradeService","put_CanAutomaticallyUpgradeService","wua.iupdatesearchercanautomaticallyupgradeservice","wuapi/IUpdateSearcher::CanAutomaticallyUpgradeService","wuapi/IUpdateSearcher::get_CanAutomaticallyUpgradeService","wuapi/IUpdateSearcher::put_CanAutomaticallyUpgradeService"]
old-location: wua\iupdatesearchercanautomaticallyupgradeservice.htm
tech.root: wua
ms.assetid: 115a637d-0b70-4d33-a9c1-43d2faf79067
ms.date: 12/05/2018
ms.keywords: CanAutomaticallyUpgradeService property [Windows Update Agent], CanAutomaticallyUpgradeService property [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],CanAutomaticallyUpgradeService property, IUpdateSearcher.CanAutomaticallyUpgradeService, IUpdateSearcher.put_CanAutomaticallyUpgradeService, IUpdateSearcher::CanAutomaticallyUpgradeService, IUpdateSearcher::get_CanAutomaticallyUpgradeService, IUpdateSearcher::put_CanAutomaticallyUpgradeService, put_CanAutomaticallyUpgradeService, wua.iupdatesearchercanautomaticallyupgradeservice, wuapi/IUpdateSearcher::CanAutomaticallyUpgradeService, wuapi/IUpdateSearcher::get_CanAutomaticallyUpgradeService, wuapi/IUpdateSearcher::put_CanAutomaticallyUpgradeService
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateSearcher::put_CanAutomaticallyUpgradeService
 - wuapi/IUpdateSearcher::put_CanAutomaticallyUpgradeService
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher.CanAutomaticallyUpgradeService
 - IUpdateSearcher.get_CanAutomaticallyUpgradeService
 - IUpdateSearcher.put_CanAutomaticallyUpgradeService
---

# IUpdateSearcher::put_CanAutomaticallyUpgradeService


## -description

Gets and sets a Boolean value that indicates whether future calls to the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">BeginSearch</a> and <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-search">Search</a> methods result in an automatic upgrade to Windows Update Agent (WUA). Currently, this property's valid value corresponds to the option that does not automatically upgrade  WUA.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>

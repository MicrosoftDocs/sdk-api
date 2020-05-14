---
UID: NF:wuapi.IUpdateSearcher.get_CanAutomaticallyUpgradeService
title: IUpdateSearcher::get_CanAutomaticallyUpgradeService (wuapi.h)
description: Gets and sets a Boolean value that indicates whether future calls to the BeginSearch and Search methods result in an automatic upgrade to Windows Update Agent (WUA).helpviewer_keywords: ["CanAutomaticallyUpgradeService property [Windows Update Agent]","CanAutomaticallyUpgradeService property [Windows Update Agent]","IUpdateSearcher interface","IUpdateSearcher interface [Windows Update Agent]","CanAutomaticallyUpgradeService property","IUpdateSearcher.CanAutomaticallyUpgradeService","IUpdateSearcher.get_CanAutomaticallyUpgradeService","IUpdateSearcher::CanAutomaticallyUpgradeService","IUpdateSearcher::get_CanAutomaticallyUpgradeService","IUpdateSearcher::put_CanAutomaticallyUpgradeService","get_CanAutomaticallyUpgradeService","wua.iupdatesearchercanautomaticallyupgradeservice","wuapi/IUpdateSearcher::CanAutomaticallyUpgradeService","wuapi/IUpdateSearcher::get_CanAutomaticallyUpgradeService","wuapi/IUpdateSearcher::put_CanAutomaticallyUpgradeService"]
old-location: wua\iupdatesearchercanautomaticallyupgradeservice.htm
tech.root: Wua_Sdk
ms.assetid: 115a637d-0b70-4d33-a9c1-43d2faf79067
ms.date: 12/05/2018
ms.keywords: CanAutomaticallyUpgradeService property [Windows Update Agent], CanAutomaticallyUpgradeService property [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],CanAutomaticallyUpgradeService property, IUpdateSearcher.CanAutomaticallyUpgradeService, IUpdateSearcher.get_CanAutomaticallyUpgradeService, IUpdateSearcher::CanAutomaticallyUpgradeService, IUpdateSearcher::get_CanAutomaticallyUpgradeService, IUpdateSearcher::put_CanAutomaticallyUpgradeService, get_CanAutomaticallyUpgradeService, wua.iupdatesearchercanautomaticallyupgradeservice, wuapi/IUpdateSearcher::CanAutomaticallyUpgradeService, wuapi/IUpdateSearcher::get_CanAutomaticallyUpgradeService, wuapi/IUpdateSearcher::put_CanAutomaticallyUpgradeService
f1_keywords:
- wuapi/IUpdateSearcher.CanAutomaticallyUpgradeService
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUpdateSearcher::get_CanAutomaticallyUpgradeService


## -description


Gets and sets a Boolean value that indicates whether future calls to the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">BeginSearch</a> and <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-search">Search</a> methods result in an automatic upgrade to Windows Update Agent (WUA). Currently, this property's valid value corresponds to the option that does not automatically upgrade  WUA.

This property is read/write.


## -parameters


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>
 

 


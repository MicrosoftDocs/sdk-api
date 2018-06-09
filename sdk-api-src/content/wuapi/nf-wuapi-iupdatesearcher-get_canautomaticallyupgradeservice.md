---
UID: NF:wuapi.IUpdateSearcher.get_CanAutomaticallyUpgradeService
title: IUpdateSearcher::get_CanAutomaticallyUpgradeService
author: windows-sdk-content
description: Gets and sets a Boolean value that indicates whether future calls to the BeginSearch and Search methods result in an automatic upgrade to Windows Update Agent (WUA).
old-location: wua\iupdatesearchercanautomaticallyupgradeservice.htm
old-project: Wua_Sdk
ms.assetid: 115a637d-0b70-4d33-a9c1-43d2faf79067
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CanAutomaticallyUpgradeService property [Windows Update Agent], CanAutomaticallyUpgradeService property [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],CanAutomaticallyUpgradeService property, IUpdateSearcher.CanAutomaticallyUpgradeService, IUpdateSearcher.get_CanAutomaticallyUpgradeService, IUpdateSearcher::CanAutomaticallyUpgradeService, IUpdateSearcher::get_CanAutomaticallyUpgradeService, IUpdateSearcher::put_CanAutomaticallyUpgradeService, get_CanAutomaticallyUpgradeService, wua.iupdatesearchercanautomaticallyupgradeservice, wuapi/IUpdateSearcher::CanAutomaticallyUpgradeService, wuapi/IUpdateSearcher::get_CanAutomaticallyUpgradeService, wuapi/IUpdateSearcher::put_CanAutomaticallyUpgradeService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UpdateType
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
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateSearcher::get_CanAutomaticallyUpgradeService


## -description


Gets and sets a Boolean value that indicates whether future calls to the <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">BeginSearch</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/mt219145">Search</a> methods result in an automatic upgrade to Windows Update Agent (WUA). Currently, this property's valid value corresponds to the option that does not automatically upgrade  WUA.

This property is read/write.


## -parameters


## -see-also




<a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>
 

 


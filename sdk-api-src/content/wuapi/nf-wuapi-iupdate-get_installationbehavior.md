---
UID: NF:wuapi.IUpdate.get_InstallationBehavior
title: IUpdate::get_InstallationBehavior
author: windows-sdk-content
description: Gets an interface that contains the installation options of the update.
old-location: wua\iupdate_installationbehavior.htm
old-project: Wua_Sdk
ms.assetid: f02e5ebc-a8ea-496b-a79e-52644b98e75d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IUpdate interface [Windows Update Agent],InstallationBehavior property, IUpdate.InstallationBehavior, IUpdate.get_InstallationBehavior, IUpdate::InstallationBehavior, IUpdate::get_InstallationBehavior, InstallationBehavior property [Windows Update Agent], InstallationBehavior property [Windows Update Agent],IUpdate interface, get_InstallationBehavior, wua.iupdate_installationbehavior, wuapi/IUpdate::InstallationBehavior, wuapi/IUpdate::get_InstallationBehavior
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdate.InstallationBehavior
-	IUpdate.get_InstallationBehavior
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdate::get_InstallationBehavior


## -description


Gets an interface that contains the installation options of the update.

This property is read-only.


## -parameters


## -remarks



If the current update represents a bundle, the <b>InstallationBehavior</b> property of the bundle will be determined by the <b>InstallationBehavior</b> property of the child updates of the bundle.




## -see-also




<a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a>
 

 


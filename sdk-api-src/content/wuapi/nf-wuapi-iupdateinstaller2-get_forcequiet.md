---
UID: NF:wuapi.IUpdateInstaller2.get_ForceQuiet
title: IUpdateInstaller2::get_ForceQuiet
author: windows-sdk-content
description: Gets and sets a Boolean value that indicates whether Windows Installer is forced to install the updates without user interaction.
old-location: wua\iupdateinstaller2_forcequiet.htm
tech.root: wua_sdk
ms.assetid: 762da3b9-8fb6-44a6-bce2-df8f15a6db0b
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ForceQuiet property [Windows Update Agent], ForceQuiet property [Windows Update Agent],IUpdateInstaller2 interface, IUpdateInstaller2 interface [Windows Update Agent],ForceQuiet property, IUpdateInstaller2.ForceQuiet, IUpdateInstaller2.get_ForceQuiet, IUpdateInstaller2::ForceQuiet, IUpdateInstaller2::get_ForceQuiet, IUpdateInstaller2::put_ForceQuiet, get_ForceQuiet, wua.iupdateinstaller2_forcequiet, wuapi/IUpdateInstaller2::ForceQuiet, wuapi/IUpdateInstaller2::get_ForceQuiet, wuapi/IUpdateInstaller2::put_ForceQuiet
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUpdateInstaller2.ForceQuiet
 - IUpdateInstaller2.get_ForceQuiet
 - IUpdateInstaller2.put_ForceQuiet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUpdateInstaller2::get_ForceQuiet


## -description


Gets and sets a Boolean value that indicates whether Windows Installer is forced to install the updates without user interaction.

This property is read/write.


## -parameters


## -remarks



You cannot forcibly silence some updates. If an update does not support this action, and you try to install the update, the update returns the following: WU_E_UH_DOESNOTSUPPORTACTION.




## -see-also




<a href="https://msdn.microsoft.com/89edc91d-59a1-4e23-9adb-fc3027e2e898">IUpdateInstaller2</a>
 

 


---
UID: NF:wuapi.IUpdateInstaller3.get_AttemptCloseAppsIfNecessary
title: IUpdateInstaller3::get_AttemptCloseAppsIfNecessary
author: windows-sdk-content
description: Gets a value indicating whether the update installer will attempt to close applications, blocking immediate installation of updates.
old-location: wua\iupdateinstaller3_get_attemptcloseappsifnecessary.htm
old-project: wua_sdk
ms.assetid: ACC9EBDD-E050-41B7-82EF-186094750DCA
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUpdateInstaller3 interface [Windows Update Agent],get_AttemptCloseAppsIfNecessary method, IUpdateInstaller3.get_AttemptCloseAppsIfNecessary, IUpdateInstaller3::get_AttemptCloseAppsIfNecessary, get_AttemptCloseAppsIfNecessary, get_AttemptCloseAppsIfNecessary method [Windows Update Agent], get_AttemptCloseAppsIfNecessary method [Windows Update Agent],IUpdateInstaller3 interface, wua.iupdateinstaller3_get_attemptcloseappsifnecessary, wuapi/IUpdateInstaller3::get_AttemptCloseAppsIfNecessary
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1803 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
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
 - IUpdateInstaller3.get_AttemptCloseAppsIfNecessary
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateInstaller3::get_AttemptCloseAppsIfNecessary


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]
<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Gets a value indicating whether the update installer will attempt to close applications, blocking immediate installation of updates.


## -parameters




### -param retval [out]

True if the installer will attempt to close applications.


## -returns



Returns S_OK on success.




## -see-also




<a href="wua.iupdateinstaller3">IUpdateInstaller3</a>
 

 


---
UID: NF:wuapi.IUpdateInstaller3.put_AttemptCloseAppsIfNecessary
title: IUpdateInstaller3::put_AttemptCloseAppsIfNecessary (wuapi.h)
description: Sets a value indicating whether the update installer will attempt to close applications, blocking immediate installation of updates.
helpviewer_keywords: ["IUpdateInstaller3 interface [Windows Update Agent]","put_AttemptCloseAppsIfNecessary method","IUpdateInstaller3.put_AttemptCloseAppsIfNecessary","IUpdateInstaller3::put_AttemptCloseAppsIfNecessary","put_AttemptCloseAppsIfNecessary","put_AttemptCloseAppsIfNecessary method [Windows Update Agent]","put_AttemptCloseAppsIfNecessary method [Windows Update Agent]","IUpdateInstaller3 interface","wua.iupdateinstaller3_put_attemptcloseappsifnecessary","wuapi/IUpdateInstaller3::put_AttemptCloseAppsIfNecessary"]
old-location: wua\iupdateinstaller3_put_attemptcloseappsifnecessary.htm
tech.root: wua
ms.assetid: 3D6F1FED-0A5A-4D6F-ACE1-BA233F5AED2E
ms.date: 12/05/2018
ms.keywords: IUpdateInstaller3 interface [Windows Update Agent],put_AttemptCloseAppsIfNecessary method, IUpdateInstaller3.put_AttemptCloseAppsIfNecessary, IUpdateInstaller3::put_AttemptCloseAppsIfNecessary, put_AttemptCloseAppsIfNecessary, put_AttemptCloseAppsIfNecessary method [Windows Update Agent], put_AttemptCloseAppsIfNecessary method [Windows Update Agent],IUpdateInstaller3 interface, wua.iupdateinstaller3_put_attemptcloseappsifnecessary, wuapi/IUpdateInstaller3::put_AttemptCloseAppsIfNecessary
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
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateInstaller3::put_AttemptCloseAppsIfNecessary
 - wuapi/IUpdateInstaller3::put_AttemptCloseAppsIfNecessary
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
 - IUpdateInstaller3.put_AttemptCloseAppsIfNecessary
---

# IUpdateInstaller3::put_AttemptCloseAppsIfNecessary


## -description


<p class="CCE_Message">[This method is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Sets a value indicating whether the update installer will attempt to close applications, blocking immediate installation of updates.

## -parameters

### -param value

Set to True if the installer should attempt to close applications.

## -returns

Returns S_OK on success.

## -see-also

<a href="nn-wuapi-iupdateinstaller3.md">IUpdateInstaller3</a>


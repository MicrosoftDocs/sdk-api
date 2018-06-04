---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WSB_OB_REGISTRATION_INFO structure


## -description


 The <b>WSB_OB_REGISTRATION_INFO</b> structure contains information to register a cloud backup provider with Windows Server Backup.


## -struct-fields




### -field m_wszResourceDLL

The complete path to the resource DLL where the provider name and icon resources can be loaded from.


### -field m_guidSnapinId

The snap-in identifier of the cloud backup provider to be registered with Windows Server Backup.


### -field m_dwProviderName

The resource identifier of the cloud backup provider name. This name will be shown in the Windows Server Backup MMC  snap-in.


### -field m_dwProviderIcon

The resource identifier of the cloud backup provider icon. This icon will be shown in the Windows Server Backup MMC snap-in.


### -field m_bSupportsRemoting

A flag to indicate whether the cloud backup provider can communicate with a remote cloud backup provider engine.


## -see-also




<a href="https://msdn.microsoft.com/C1AC87C6-37B7-4675-AB51-45C292239EB5">Cloud  Backup Provider API Structures</a>



<a href="https://msdn.microsoft.com/F6BBE44C-E735-47E9-8AD1-A7F1FBAC0330">RegisterOnlineBackupWithWindowsServerBackup</a>
 

 


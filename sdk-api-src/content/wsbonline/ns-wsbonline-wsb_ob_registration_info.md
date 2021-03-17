---
UID: NS:wsbonline._WSB_OB_REGISTRATION_INFO
title: WSB_OB_REGISTRATION_INFO (wsbonline.h)
description: Contains information to register a cloud backup provider with Windows Server Backup.
helpviewer_keywords: ["WSB_OB_REGISTRATION_INFO","WSB_OB_REGISTRATION_INFO structure [Windows Server Backup]","wsb.wsb_ob_registration_info","wsbonline/WSB_OB_REGISTRATION_INFO"]
old-location: wsb\wsb_ob_registration_info.htm
tech.root: wsb
ms.assetid: E01EF90E-90F1-4B56-85B8-63A10A688FBA
ms.date: 12/05/2018
ms.keywords: WSB_OB_REGISTRATION_INFO, WSB_OB_REGISTRATION_INFO structure [Windows Server Backup], wsb.wsb_ob_registration_info, wsbonline/WSB_OB_REGISTRATION_INFO
req.header: wsbonline.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
req.typenames: WSB_OB_REGISTRATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSB_OB_REGISTRATION_INFO
 - wsbonline/_WSB_OB_REGISTRATION_INFO
 - WSB_OB_REGISTRATION_INFO
 - wsbonline/WSB_OB_REGISTRATION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsbOnline.h
api_name:
 - WSB_OB_REGISTRATION_INFO
---

# WSB_OB_REGISTRATION_INFO structure


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

<a href="/previous-versions/windows/desktop/wsb/windows-server-backup-api-structures">Cloud  Backup Provider API Structures</a>



<a href="/previous-versions/windows/desktop/api/wsbonline/nf-wsbonline-registeronlinebackupwithwindowsserverbackup">RegisterOnlineBackupWithWindowsServerBackup</a>
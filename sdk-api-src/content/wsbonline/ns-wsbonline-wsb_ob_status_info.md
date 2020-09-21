---
UID: NS:wsbonline._WSB_OB_STATUS_INFO
title: WSB_OB_STATUS_INFO (wsbonline.h)
description: Contains information to update the cloud backup provider status in the Windows Server Backup MMC snap-in.
helpviewer_keywords: ["WSB_OB_STATUS_INFO","WSB_OB_STATUS_INFO structure [Windows Server Backup]","wsb.wsb_ob_status_info","wsbonline/WSB_OB_STATUS_INFO"]
old-location: wsb\wsb_ob_status_info.htm
tech.root: wsb
ms.assetid: 5836B3FC-5590-4678-A6BE-AD7C59E0FAFD
ms.date: 12/05/2018
ms.keywords: WSB_OB_STATUS_INFO, WSB_OB_STATUS_INFO structure [Windows Server Backup], wsb.wsb_ob_status_info, wsbonline/WSB_OB_STATUS_INFO
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
req.typenames: WSB_OB_STATUS_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSB_OB_STATUS_INFO
 - wsbonline/_WSB_OB_STATUS_INFO
 - WSB_OB_STATUS_INFO
 - wsbonline/WSB_OB_STATUS_INFO
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
 - WSB_OB_STATUS_INFO
---

# WSB_OB_STATUS_INFO structure


## -description

 The <b>WSB_OB_STATUS_INFO</b> structure contains information to update the cloud backup provider status in the Windows Server Backup MMC snap-in.

## -struct-fields

### -field m_guidSnapinId

The snap-in identifier of the cloud backup provider registered with Windows Server Backup.

### -field m_cStatusEntry

The number of status entries contained in the <b>m_rgStatusEntry</b> member. The maximum number of entries allowed is five.

### -field m_rgStatusEntry

A pointer to one or more <a href="/windows/desktop/api/wsbonline/ns-wsbonline-wsb_ob_status_entry">WSB_OB_STATUS_ENTRY</a> structures, each  containing cloud backup provider status information  for one entry to be shown in the Windows Server Backup MMC snap-in.

## -see-also

<a href="/previous-versions/windows/desktop/wsb/windows-server-backup-api-structures">Cloud  Backup Provider API Structures</a>



<a href="/previous-versions/windows/desktop/api/wsbonline/nf-wsbonline-updateobstatusinwindowsserverbackup">UpdateOBStatusInWindowsServerBackup</a>



<a href="/windows/desktop/api/wsbonline/ns-wsbonline-wsb_ob_status_entry">WSB_OB_STATUS_ENTRY</a>
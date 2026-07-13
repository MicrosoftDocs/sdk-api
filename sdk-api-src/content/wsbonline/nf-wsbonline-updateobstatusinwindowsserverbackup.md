---
UID: NF:wsbonline.UpdateOBStatusInWindowsServerBackup
title: UpdateOBStatusInWindowsServerBackup function (wsbonline.h)
description: Updates the Cloud backup provider status in the Windows Server Backup MMC snap-in.
helpviewer_keywords: ["UpdateOBStatusInWindowsServerBackup","UpdateOBStatusInWindowsServerBackup function [Windows Server Backup]","wsb.updateobstatusinwindowsserverbackup","wsbonline/UpdateOBStatusInWindowsServerBackup"]
old-location: wsb\updateobstatusinwindowsserverbackup.htm
tech.root: wsb
ms.assetid: 13C745FB-D0B9-432E-BDBA-E4194BF54924
ms.date: 12/05/2018
ms.keywords: UpdateOBStatusInWindowsServerBackup, UpdateOBStatusInWindowsServerBackup function [Windows Server Backup], wsb.updateobstatusinwindowsserverbackup, wsbonline/UpdateOBStatusInWindowsServerBackup
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
req.lib: wsbonline.lib
req.dll: WsbOnline.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UpdateOBStatusInWindowsServerBackup
 - wsbonline/UpdateOBStatusInWindowsServerBackup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsbOnline.dll
api_name:
 - UpdateOBStatusInWindowsServerBackup
---

# UpdateOBStatusInWindowsServerBackup function


## -description

The <b>UpdateOBStatusInWindowsServerBackup</b> function updates the cloud backup provider status in the Windows Server Backup MMC snap-in.

## -parameters

### -param pOBRegistrationInfo [in]

Pointer to a <a href="/windows/desktop/api/wsbonline/ns-wsbonline-wsb_ob_status_info">WSB_OB_STATUS_INFO</a> structure.

## -returns

The return values listed here are in addition to the normal <b>HRESULT</b>s that may be returned at any time 
       from the function.

## -see-also

<a href="/previous-versions/windows/desktop/wsb/windows-server-backup-api-functions">Cloud  Backup Provider API Functions</a>



<a href="/windows/desktop/api/wsbonline/ns-wsbonline-wsb_ob_status_info">WSB_OB_STATUS_INFO</a>
---
UID: NS:wsbonline._WSB_OB_STATUS_INFO
title: "_WSB_OB_STATUS_INFO"
author: windows-sdk-content
description: Contains information to update the cloud backup provider status in the Windows Server Backup MMC snap-in.
old-location: wsb\wsb_ob_status_info.htm
tech.root: wsb
ms.assetid: 5836B3FC-5590-4678-A6BE-AD7C59E0FAFD
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WSB_OB_STATUS_INFO, WSB_OB_STATUS_INFO structure [Windows Server Backup], _WSB_OB_STATUS_INFO, wsb.wsb_ob_status_info, wsbonline/WSB_OB_STATUS_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WsbOnline.h
api_name:
 - WSB_OB_STATUS_INFO
product: Windows
targetos: Windows
req.typenames: WSB_OB_STATUS_INFO
req.redist: 
---

# _WSB_OB_STATUS_INFO structure


## -description


 The <b>WSB_OB_STATUS_INFO</b> structure contains information to update the cloud backup provider status in the Windows Server Backup MMC snap-in.


## -struct-fields




### -field m_guidSnapinId

The snap-in identifier of the cloud backup provider registered with Windows Server Backup.


### -field m_cStatusEntry

The number of status entries contained in the <b>m_rgStatusEntry</b> member. The maximum number of entries allowed is five.


### -field m_rgStatusEntry

A pointer to one or more <a href="https://msdn.microsoft.com/BFC13B54-60F3-43A1-B464-D09DD96F57FA">WSB_OB_STATUS_ENTRY</a> structures, each  containing cloud backup provider status information  for one entry to be shown in the Windows Server Backup MMC snap-in.


## -see-also




<a href="https://msdn.microsoft.com/C1AC87C6-37B7-4675-AB51-45C292239EB5">Cloud  Backup Provider API Structures</a>



<a href="https://msdn.microsoft.com/13C745FB-D0B9-432E-BDBA-E4194BF54924">UpdateOBStatusInWindowsServerBackup</a>



<a href="https://msdn.microsoft.com/BFC13B54-60F3-43A1-B464-D09DD96F57FA">WSB_OB_STATUS_ENTRY</a>
 

 


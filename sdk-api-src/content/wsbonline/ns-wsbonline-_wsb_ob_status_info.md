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
 

 


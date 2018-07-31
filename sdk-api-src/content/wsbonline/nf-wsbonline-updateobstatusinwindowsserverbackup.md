---
UID: NF:wsbonline.UpdateOBStatusInWindowsServerBackup
title: UpdateOBStatusInWindowsServerBackup function
author: windows-sdk-content
description: Updates the Cloud backup provider status in the Windows Server Backup MMC snap-in.
old-location: wsb\updateobstatusinwindowsserverbackup.htm
old-project: wsb
ms.assetid: 13C745FB-D0B9-432E-BDBA-E4194BF54924
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: UpdateOBStatusInWindowsServerBackup, UpdateOBStatusInWindowsServerBackup function [Windows Server Backup], wsb.updateobstatusinwindowsserverbackup, wsbonline/UpdateOBStatusInWindowsServerBackup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: WSB_OB_STATUS_ENTRY_PAIR_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsbOnline.dll
api_name:
 - UpdateOBStatusInWindowsServerBackup
product: Windows
targetos: Windows
req.lib: 
req.dll: WsbOnline.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# UpdateOBStatusInWindowsServerBackup function


## -description


The <b>UpdateOBStatusInWindowsServerBackup</b> function updates the cloud backup provider status in the Windows Server Backup MMC snap-in.


## -parameters




### -param pOBRegistrationInfo [in]

Pointer to a <a href="https://msdn.microsoft.com/5836B3FC-5590-4678-A6BE-AD7C59E0FAFD">WSB_OB_STATUS_INFO</a> structure.


## -returns



The return values listed here are in addition to the normal <b>HRESULT</b>s that may be returned at any time 
       from the function.




## -see-also




<a href="https://msdn.microsoft.com/61F77E92-19EF-4409-9435-CD03ACCE810D">Cloud  Backup Provider API Functions</a>



<a href="https://msdn.microsoft.com/5836B3FC-5590-4678-A6BE-AD7C59E0FAFD">WSB_OB_STATUS_INFO</a>
 

 


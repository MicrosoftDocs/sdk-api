---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyBlockProgress
title: IDiscMasterProgressEvents::NotifyBlockProgress method
author: windows-driver-content
description: Notifies an application of its progress in burning a disc on the active recorder. Notifications are sent for the first and last blocks, and at points in between.
old-location: imapi\idiscmasterprogressevents_notifyblockprogress.htm
old-project: imapi
ms.assetid: 6c156be7-5ba4-48e7-a0d1-b0b8d69b30e2
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDiscMasterProgressEvents, IDiscMasterProgressEvents interface [IMAPI], NotifyBlockProgress method, IDiscMasterProgressEvents::NotifyBlockProgress, NotifyBlockProgress method [IMAPI], NotifyBlockProgress method [IMAPI], IDiscMasterProgressEvents interface, NotifyBlockProgress,IDiscMasterProgressEvents.NotifyBlockProgress, _win32_idiscmasterprogressevents_notifyblockprogress, base.idiscmasterprogressevents_notifyblockprogress, imapi.idiscmasterprogressevents_notifyblockprogress, imapi/IDiscMasterProgressEvents::NotifyBlockProgress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IDiscMasterProgressEvents.NotifyBlockProgress
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMasterProgressEvents::NotifyBlockProgress method


## -description


Notifies an application of its progress in burning a disc on the active recorder. Notifications are sent for the first and last blocks, and at points in between.


## -parameters




### -param nCompleted [in]

Number of blocks that have been burned onto a disc or track so far.


### -param nTotal [in]

Total number of blocks to be burned to finish a disc or track.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a>
 

 


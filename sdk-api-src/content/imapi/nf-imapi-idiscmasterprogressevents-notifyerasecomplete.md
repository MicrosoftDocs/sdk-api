---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyEraseComplete
title: IDiscMasterProgressEvents::NotifyEraseComplete method
author: windows-driver-content
description: Notifies an application that a call to IDiscRecorder::Erase has finished.
old-location: imapi\idiscmasterprogressevents_notifyerasecomplete.htm
old-project: imapi
ms.assetid: 17a0debe-919d-4db7-bcbb-eb4fc9973d83
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IDiscMasterProgressEvents, IDiscMasterProgressEvents interface [IMAPI], NotifyEraseComplete method, IDiscMasterProgressEvents::NotifyEraseComplete, NotifyEraseComplete method [IMAPI], NotifyEraseComplete method [IMAPI], IDiscMasterProgressEvents interface, NotifyEraseComplete,IDiscMasterProgressEvents.NotifyEraseComplete, _win32_idiscmasterprogressevents_notifyerasecomplete, base.idiscmasterprogressevents_notifyerasecomplete, imapi.idiscmasterprogressevents_notifyerasecomplete, imapi/IDiscMasterProgressEvents::NotifyEraseComplete
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
-	IDiscMasterProgressEvents.NotifyEraseComplete
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMasterProgressEvents::NotifyEraseComplete method


## -description


Notifies an application that a call to 
<a href="https://msdn.microsoft.com/61a9cada-a9f4-462d-ab73-a9319308ff01">IDiscRecorder::Erase</a> has finished.


## -parameters




### -param status [in]

Status code to be returned from 
<a href="https://msdn.microsoft.com/61a9cada-a9f4-462d-ab73-a9319308ff01">IDiscRecorder::Erase</a>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a>
 

 


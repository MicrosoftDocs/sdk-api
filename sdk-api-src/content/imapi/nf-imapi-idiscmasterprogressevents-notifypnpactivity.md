---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyPnPActivity
title: IDiscMasterProgressEvents::NotifyPnPActivity
author: windows-sdk-content
description: Notifies the application that there is a change to the list of valid disc recorders. (For example, a USB CD-R driver is removed from the system.).
old-location: imapi\idiscmasterprogressevents_notifypnpactivity.htm
old-project: imapi
ms.assetid: d2b41e86-2f1b-46f1-955d-7fc42f8189a4
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyPnPActivity method, IDiscMasterProgressEvents.NotifyPnPActivity, IDiscMasterProgressEvents::NotifyPnPActivity, NotifyPnPActivity, NotifyPnPActivity method [IMAPI], NotifyPnPActivity method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifypnpactivity, base.idiscmasterprogressevents_notifypnpactivity, imapi.idiscmasterprogressevents_notifypnpactivity, imapi/IDiscMasterProgressEvents::NotifyPnPActivity
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IDiscMasterProgressEvents.NotifyPnPActivity
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMasterProgressEvents::NotifyPnPActivity


## -description


Notifies the application that there is a change to the list of valid disc recorders. (For example, a USB CD-R driver is removed from the system.)


## -parameters






## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



An application should respond by calling 
<a href="https://msdn.microsoft.com/03daab81-11cf-4100-ab5e-3442a5972912">IDiscMaster::EnumDiscRecorders</a> to update its list of valid recorders. If the current active recorder has been invalidated, then a new recorder should be chosen.




## -see-also




<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a>
 

 


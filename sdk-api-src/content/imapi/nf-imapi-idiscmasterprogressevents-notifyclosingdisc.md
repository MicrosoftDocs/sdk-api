---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyClosingDisc
title: IDiscMasterProgressEvents::NotifyClosingDisc
author: windows-sdk-content
description: Notifies the application that it is has started closing the disc. No further notifications are sent until the burn is finished.
old-location: imapi\idiscmasterprogressevents_notifyclosingdisc.htm
old-project: imapi
ms.assetid: 2eeccb4e-0e49-40a9-b659-f0784f921074
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyClosingDisc method, IDiscMasterProgressEvents.NotifyClosingDisc, IDiscMasterProgressEvents::NotifyClosingDisc, NotifyClosingDisc, NotifyClosingDisc method [IMAPI], NotifyClosingDisc method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifyclosingdisc, base.idiscmasterprogressevents_notifyclosingdisc, imapi.idiscmasterprogressevents_notifyclosingdisc, imapi/IDiscMasterProgressEvents::NotifyClosingDisc
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscMasterProgressEvents.NotifyClosingDisc
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMasterProgressEvents::NotifyClosingDisc


## -description


Notifies the application that it is has started closing the disc. No further notifications are sent until the burn is finished.


## -parameters




### -param nEstimatedSeconds [in]

Number of seconds from notification that IMAPI estimates it will take to close the disc.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a>
 

 


---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyPreparingBurn
title: IDiscMasterProgressEvents::NotifyPreparingBurn (imapi.h)
author: windows-sdk-content
description: Notifies the application that it is preparing to burn a disc. No further notifications are sent until the burn starts.
old-location: imapi\idiscmasterprogressevents_notifypreparingburn.htm
tech.root: imapi
ms.assetid: 28aced4e-6e7e-40fe-a00a-c0e470815cac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyPreparingBurn method, IDiscMasterProgressEvents.NotifyPreparingBurn, IDiscMasterProgressEvents::NotifyPreparingBurn, NotifyPreparingBurn, NotifyPreparingBurn method [IMAPI], NotifyPreparingBurn method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifypreparingburn, base.idiscmasterprogressevents_notifypreparingburn, imapi.idiscmasterprogressevents_notifypreparingburn, imapi/IDiscMasterProgressEvents::NotifyPreparingBurn
ms.topic: method
f1_keywords: 
 - "imapi/IDiscMasterProgressEvents.NotifyPreparingBurn"
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
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IDiscMasterProgressEvents.NotifyPreparingBurn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDiscMasterProgressEvents::NotifyPreparingBurn


## -description


Notifies the application that it is preparing to burn a disc. No further notifications are sent until the burn starts.


## -parameters




### -param nEstimatedSeconds [in]

Number of seconds from notification that IMAPI estimates it will take to prepare to burn the disc.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/imapi/nn-imapi-idiscmasterprogressevents">IDiscMasterProgressEvents</a>
 

 


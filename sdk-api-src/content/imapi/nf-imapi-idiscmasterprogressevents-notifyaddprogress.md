---
UID: NF:imapi.IDiscMasterProgressEvents.NotifyAddProgress
title: IDiscMasterProgressEvents::NotifyAddProgress
author: windows-sdk-content
description: Notifies an application of its progress in response to calls to IRedbookDiscMaster::AddAudioTrackBlocks or IJolietDiscMaster::AddData. Notifications are sent for the first and last steps, and at points in between.
old-location: imapi\idiscmasterprogressevents_notifyaddprogress.htm
tech.root: imapi
ms.assetid: d367b789-430e-48f5-9e50-5d6ffb9d7ebc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscMasterProgressEvents interface [IMAPI],NotifyAddProgress method, IDiscMasterProgressEvents.NotifyAddProgress, IDiscMasterProgressEvents::NotifyAddProgress, NotifyAddProgress, NotifyAddProgress method [IMAPI], NotifyAddProgress method [IMAPI],IDiscMasterProgressEvents interface, _win32_idiscmasterprogressevents_notifyaddprogress, base.idiscmasterprogressevents_notifyaddprogress, imapi.idiscmasterprogressevents_notifyaddprogress, imapi/IDiscMasterProgressEvents::NotifyAddProgress
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
 - IDiscMasterProgressEvents.NotifyAddProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscMasterProgressEvents::NotifyAddProgress


## -description


Notifies an application of its progress in response to calls to 
<a href="https://msdn.microsoft.com/d9bd4f3c-4ff5-4f6e-9520-27fef3736636">IRedbookDiscMaster::AddAudioTrackBlocks</a> or 
<a href="https://msdn.microsoft.com/91517103-71c5-450c-9d93-584f94cd2c45">IJolietDiscMaster::AddData</a>. Notifications are sent for the first and last steps, and at points in between.


## -parameters




### -param nCompletedSteps [in]

Number of arbitrary steps that have been completed in adding audio or data to a staged image.


### -param nTotalSteps [in]

Total number of arbitrary steps that must be taken to add a full set of audio or data to the staged image.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a>
 

 


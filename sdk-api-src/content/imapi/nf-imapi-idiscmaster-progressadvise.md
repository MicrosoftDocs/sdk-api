---
UID: NF:imapi.IDiscMaster.ProgressAdvise
title: IDiscMaster::ProgressAdvise
author: windows-sdk-content
description: Registers an application for progress notifications.
old-location: imapi\idiscmaster_progressadvise.htm
tech.root: imapi
ms.assetid: 64966230-2042-46cb-9974-adbe382723a1
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IDiscMaster interface [IMAPI],ProgressAdvise method, IDiscMaster.ProgressAdvise, IDiscMaster::ProgressAdvise, ProgressAdvise, ProgressAdvise method [IMAPI], ProgressAdvise method [IMAPI],IDiscMaster interface, _win32_idiscmaster_progressadvise, base.idiscmaster_progressadvise, imapi.idiscmaster_progressadvise, imapi/IDiscMaster::ProgressAdvise
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
 - IDiscMaster.ProgressAdvise
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscMaster::ProgressAdvise


## -description


Registers an application for progress notifications.


## -parameters




### -param pEvents [in]

Pointer to an 
<a href="https://msdn.microsoft.com/68f7edbd-4a06-4e8d-a562-21a65767aff6">IDiscMasterProgressEvents</a> interface that receives the progress notifications.


### -param pvCookie

TBD




#### - pnCookie [out]

Uniquely identifies this registration. Save this value because it will be needed by the 
<a href="https://msdn.microsoft.com/b2729ff7-aefb-40cf-ae7b-9451fbe10bbb">ProgressUnadvise</a> method.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 


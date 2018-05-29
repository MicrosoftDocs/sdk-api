---
UID: NF:imapi.IDiscMaster.GetActiveDiscRecorder
title: IDiscMaster::GetActiveDiscRecorder
author: windows-sdk-content
description: Retrieves an interface pointer to the active disc recorder. The active disc recorder is the recorder where a burn will occur when RecordDisc is called.
old-location: imapi\idiscmaster_getactivediscrecorder.htm
old-project: imapi
ms.assetid: bdbc6108-c5c9-4083-84cd-7eae63d45c0f
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: GetActiveDiscRecorder, GetActiveDiscRecorder method [IMAPI], GetActiveDiscRecorder method [IMAPI],IDiscMaster interface, IDiscMaster interface [IMAPI],GetActiveDiscRecorder method, IDiscMaster.GetActiveDiscRecorder, IDiscMaster::GetActiveDiscRecorder, _win32_idiscmaster_getactivediscrecorder, base.idiscmaster_getactivediscrecorder, imapi.idiscmaster_getactivediscrecorder, imapi/IDiscMaster::GetActiveDiscRecorder
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
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IDiscMaster.GetActiveDiscRecorder
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IDiscMaster::GetActiveDiscRecorder


## -description


Retrieves an interface pointer to the active disc recorder. The active disc recorder is the recorder where a burn will occur when 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">RecordDisc</a> is called.


## -parameters




### -param ppRecorder [out]

Pointer to the 
<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a> interface of the currently selected disc recorder.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



There is no default active disc recorder. An application using this method must specifically select both an active mastering format and an active disc recorder before initiating a burn.

<div class="alert"><b>Note</b>  The active disc recorder can be invalidated by removing the device or changing the active disc mastering format. For example, a USB CD-R device may be disconnected from the machine while the application is still running (the application is alerted to this condition by a call to 
<a href="https://msdn.microsoft.com/d2b41e86-2f1b-46f1-955d-7fc42f8189a4">IDiscMasterProgressEvents::NotifyPnPActivity</a>). In either case, you must select a new active disc recorder.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>
 

 


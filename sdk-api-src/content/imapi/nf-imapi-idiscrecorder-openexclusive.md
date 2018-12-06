---
UID: NF:imapi.IDiscRecorder.OpenExclusive
title: IDiscRecorder::OpenExclusive
author: windows-sdk-content
description: Opens a disc recorder for exclusive access.
old-location: imapi\idiscrecorder_openexclusive.htm
tech.root: imapi
ms.assetid: e704baf0-d403-4cf7-aa32-16677d9a8694
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDiscRecorder interface [IMAPI],OpenExclusive method, IDiscRecorder.OpenExclusive, IDiscRecorder::OpenExclusive, OpenExclusive, OpenExclusive method [IMAPI], OpenExclusive method [IMAPI],IDiscRecorder interface, _win32_idiscrecorder_openexclusive, base.idiscrecorder_openexclusive, imapi.idiscrecorder_openexclusive, imapi/IDiscRecorder::OpenExclusive
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
 - IDiscRecorder.OpenExclusive
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder::OpenExclusive


## -description


Opens a disc recorder for exclusive access.


## -parameters






## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



This method blocks file system access to a recorder through applications such as Explorer. The recorder must be opened with this method before it is possible to use the following methods: 
<a href="https://msdn.microsoft.com/40f9376d-5702-4dfb-a69b-0ca4fcfc8d8e">QueryMediaType</a>, 
<a href="https://msdn.microsoft.com/29a40f49-1567-4198-b682-a0e314858baf">Eject</a>, 
<a href="https://msdn.microsoft.com/61a9cada-a9f4-462d-ab73-a9319308ff01">Erase</a>, and 
<a href="https://msdn.microsoft.com/39af9413-6068-4165-8a26-509389a6d1f2">Close</a>.

It is important to close the recorder before calling 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">IDiscMaster::RecordDisc</a>, or it will fail with IMAPI_E_DEVICE_NOTACCESSIBLE. The device is exclusively committed to access through either 
<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a> or 
<a href="https://msdn.microsoft.com/1473e79e-a13a-4bc5-b80d-d8921fdc9952">IDiscMaster</a>, but not both at the same time. This is to ensure that there is no confusion regarding allowed operations and ownership of a recorder during application control or a burn.

An exclusive lock should be held for as short a time as possible. Requests that come from other operating system components are not queued for later execution. Instead, they are simply failed. This could cause confusion with users who don't think a burn is in progress.

Any time that 
<b>OpenExclusive</b> is called, it appears to the file system that the disc has been removed. When the corresponding 
<a href="https://msdn.microsoft.com/39af9413-6068-4165-8a26-509389a6d1f2">Close</a> call is made, it appears to the file system that the media has reappeared. This may cause auto-run issues.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 


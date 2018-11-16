---
UID: NF:imapi.IDiscRecorder.Erase
title: IDiscRecorder::Erase
author: windows-sdk-content
description: Attempts to erase the CD-RW media if this is a CD-RW disc recorder. Both full and quick erases are supported.
old-location: imapi\idiscrecorder_erase.htm
tech.root: imapi
ms.assetid: 61a9cada-a9f4-462d-ab73-a9319308ff01
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Erase, Erase method [IMAPI], Erase method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],Erase method, IDiscRecorder.Erase, IDiscRecorder::Erase, _win32_idiscrecorder_erase, base.idiscrecorder_erase, imapi.idiscrecorder_erase, imapi/IDiscRecorder::Erase
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
 - IDiscRecorder.Erase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi.h
: 
- IDiscRecorder.Erase
: 
---

# IDiscRecorder::Erase


## -description


Attempts to erase the CD-RW media if this is a CD-RW disc recorder. Both full and quick erases are supported.


## -parameters




### -param bFullErase [in]

Indicates the erase type. If this parameter is <b>FALSE</b>, a quick erase is performed. If this parameter is <b>TRUE</b>, a full erase is performed.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Erasing a disc can be a very lengthy operation (sometimes in excess of an hour). To receive an erase completion notification, use <a href="https://msdn.microsoft.com/17a0debe-919d-4db7-bcbb-eb4fc9973d83">IDiscMasterProgressEvents::NotifyEraseComplete</a>.

The quick option erases only the PMA, first session TOC, and the pre-gap of the first track. This erases a disc quickly (between 1 and 2 minutes depending on recorder speed), but the program area will still contain user data. A full erase, on the other hand, erases the entire disc.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 


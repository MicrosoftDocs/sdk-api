---
UID: NF:imapi.IDiscRecorder.Eject
title: IDiscRecorder::Eject
author: windows-sdk-content
description: Unlocks and ejects the tray of the disc recorder, if possible.
old-location: imapi\idiscrecorder_eject.htm
tech.root: imapi
ms.assetid: 29a40f49-1567-4198-b682-a0e314858baf
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: Eject, Eject method [IMAPI], Eject method [IMAPI],IDiscRecorder interface, IDiscRecorder interface [IMAPI],Eject method, IDiscRecorder.Eject, IDiscRecorder::Eject, _win32_idiscrecorder_eject, base.idiscrecorder_eject, imapi.idiscrecorder_eject, imapi/IDiscRecorder::Eject
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
 - IDiscRecorder.Eject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDiscRecorder::Eject


## -description


Unlocks and ejects the tray of the disc recorder, if possible.


## -parameters






## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



Not all recorders support calls to eject their media. However, this method attempts to eject media.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 


---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 


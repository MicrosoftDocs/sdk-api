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

# IRawCDImageCreator::AddSpecialPregap


## -description


Accepts the provided <b>IStream</b> object and saves the associated pointer to be used as data for the pre-gap for track 1.


## -parameters




### -param data [in, optional]

Pointer to the provided <b>IStream</b> object.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method can only be called prior to adding any tracks to the image.  The <i>data</i> stream must be at least 2 seconds (or 150 sectors) long.

The  <i>data</i> stream should not result final sector exceeding LBA 397,799 (MSF 88:25:74), as the minimal-sized track plus leadout would then exceed the MSF 89:59:74 maximum.  Additionally, it is recommended that the <a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a>  value for the first track is implicitly defined as "Audio". The resulting audio can then only be heard by playing the first track and "rewinding" back to the start of the audio disc.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>
 

 


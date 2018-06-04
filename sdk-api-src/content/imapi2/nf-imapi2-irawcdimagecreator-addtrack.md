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

# IRawCDImageCreator::AddTrack


## -description


Accepts the provided <b>IStream</b> object and saves the interface pointer as the next track in the image.


## -parameters




### -param dataType [in]

A  value, defined by  <a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a>, that indicates the type of data. <b>IMAPI_CD_SECTOR_AUDIO</b> is the only value  supported by the <b>IRawCDImageCreator::AddTrack</b>  method.


### -param data [in, optional]

Pointer to the provided <b>IStream</b> object.


### -param trackIndex [out, retval]

A <b>LONG</b> value within a 1 to 99 range that will be associated with the new track.  


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



Any additional tracks must be compatible with all existing tracks.  See the <a href="https://msdn.microsoft.com/3af4a8c9-66b7-490e-aafa-fdfe614f5f3e">IMAPI_CD_SECTOR_TYPE</a> enumeration for  information on limitations.

The data stream must be at least 4 seconds (300 sectors) long.  Data stream may not cause final sector to exceed LBA 398,099 (MSF 88:29:74), as leadout would then exceed the MSF 89:59:74 maximum.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>
 

 


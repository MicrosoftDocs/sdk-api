---
UID: NF:imapi2.IRawCDImageCreator.get_LastUsedUserSectorInImage
title: IRawCDImageCreator::get_LastUsedUserSectorInImage
author: windows-sdk-content
description: Retrieves the number of total used sectors on the current media, including any overhead between existing tracks.
old-location: imapi\irawcdimagecreator_get_lastusedusersectorinimage.htm
tech.root: imapi
ms.assetid: 4a6b907a-2475-48c8-afd7-e212144bc165
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_LastUsedUserSectorInImage method, IRawCDImageCreator.get_LastUsedUserSectorInImage, IRawCDImageCreator::get_LastUsedUserSectorInImage, get_LastUsedUserSectorInImage, get_LastUsedUserSectorInImage method [IMAPI], get_LastUsedUserSectorInImage method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_lastusedusersectorinimage, imapi2/IRawCDImageCreator::get_LastUsedUserSectorInImage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageCreator.get_LastUsedUserSectorInImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageCreator::get_LastUsedUserSectorInImage


## -description


Retrieves the number of total used sectors on the current media, including any overhead between existing tracks.


## -parameters




### -param value [out]

Pointer to a <b>LONG</b> value that indicates the number of total used sectors on the media. 


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This value represents the LBA of the last sector with data that is considered part of a track, and does not include the overhead of the leadin, leadout, or the two-seconds between MSF 00:00:00 and MSF 00:02:00.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>
 

 


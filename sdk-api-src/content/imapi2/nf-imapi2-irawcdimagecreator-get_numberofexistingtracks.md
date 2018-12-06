---
UID: NF:imapi2.IRawCDImageCreator.get_NumberOfExistingTracks
title: IRawCDImageCreator::get_NumberOfExistingTracks
author: windows-sdk-content
description: Retrieves the number of existing audio tracks on the media.
old-location: imapi\irawcdimagecreator_get_numberofexistingtracks.htm
tech.root: imapi
ms.assetid: c10053d0-d9c1-4ac0-aa38-71dacf1e4425
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_NumberOfExistingTracks method, IRawCDImageCreator.get_NumberOfExistingTracks, IRawCDImageCreator::get_NumberOfExistingTracks, get_NumberOfExistingTracks, get_NumberOfExistingTracks method [IMAPI], get_NumberOfExistingTracks method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_numberofexistingtracks, imapi2/IRawCDImageCreator::get_NumberOfExistingTracks
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
 - IRawCDImageCreator.get_NumberOfExistingTracks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawCDImageCreator::get_NumberOfExistingTracks


## -description


Retrieves the number of existing audio tracks on the media.


## -parameters




### -param value [out]

Pointer to a <b>LONG</b> value that indicates the number of audio tracks that currently exist on the media.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>
 

 


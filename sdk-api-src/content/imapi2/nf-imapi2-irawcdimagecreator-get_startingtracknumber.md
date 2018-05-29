---
UID: NF:imapi2.IRawCDImageCreator.get_StartingTrackNumber
title: IRawCDImageCreator::get_StartingTrackNumber
author: windows-sdk-content
description: Retrieves the starting track number.
old-location: imapi\irawcdimagecreator_get_startingtracknumber.htm
old-project: imapi
ms.assetid: 307ef0b4-80b2-46c1-acca-1ce5d2222eb7
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_StartingTrackNumber method, IRawCDImageCreator.get_StartingTrackNumber, IRawCDImageCreator::get_StartingTrackNumber, get_StartingTrackNumber, get_StartingTrackNumber method [IMAPI], get_StartingTrackNumber method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_startingtracknumber, imapi2/IRawCDImageCreator::get_StartingTrackNumber
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IRawCDImageCreator.get_StartingTrackNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IRawCDImageCreator::get_StartingTrackNumber


## -description


Retrieves the starting track number.


## -parameters




### -param value [out]

Pointer to a <b>LONG</b> value that represents the starting track number.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



If this property holds a  value other than 1, all tracks added to the image must be audio tracks.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/38d1319b-0350-41bf-8984-fbeb4f5f3204">IRawCDImageCreator::put_StartingTrackNumber</a>
 

 


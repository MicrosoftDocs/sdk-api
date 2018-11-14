---
UID: NF:imapi2.IRawCDImageCreator.get_ResultingImageType
title: IRawCDImageCreator::get_ResultingImageType
author: windows-sdk-content
description: Retrieves the value that specifies the type of image file that will be generated.
old-location: imapi\irawcdimagecreator_get_resultingimagetype.htm
tech.root: imapi
ms.assetid: 006486f7-f766-44a1-a088-71035567a75d
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],get_ResultingImageType method, IRawCDImageCreator.get_ResultingImageType, IRawCDImageCreator::get_ResultingImageType, get_ResultingImageType, get_ResultingImageType method [IMAPI], get_ResultingImageType method [IMAPI],IRawCDImageCreator interface, imapi.irawcdimagecreator_get_resultingimagetype, imapi2/IRawCDImageCreator::get_ResultingImageType
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
 - IRawCDImageCreator.get_ResultingImageType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2.h
: 
- IRawCDImageCreator.get_ResultingImageType
: 
---

# IRawCDImageCreator::get_ResultingImageType


## -description


Retrieves the value that specifies the type of image file that will be generated.


## -parameters




### -param value [out]

Pointer to an <a href="https://msdn.microsoft.com/f3193377-5410-4cd2-b7e5-281b3794c583">IMAPI_FORMAT2_RAW_CD_DATA_SECTOR_TYPE</a> enumeration that defines the current type set for the  image file.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/1800717a-3b8a-45b2-849b-55c37d3b1b32">IRawCDImageCreator::put_ResultingImageType</a>
 

 


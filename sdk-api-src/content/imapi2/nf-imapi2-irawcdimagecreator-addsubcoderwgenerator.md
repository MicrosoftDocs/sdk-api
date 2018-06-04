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

# IRawCDImageCreator::AddSubcodeRWGenerator


## -description


Allows the addition of custom R-W subcode, provided by the <b>IStream</b>. The provided object must  have a size equal to the number of sectors in the raw disc image * 96 bytes when the final image is created.


## -parameters




### -param subcode [in, optional]

The subcode data (with 96 bytes per sector), where the 2 most significant bits must always be zero (as they are the P/Q bits).


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



May be added anytime prior to calling <a href="https://msdn.microsoft.com/a83293f6-d5a1-49e2-884b-2b185516109d">IRawCDImageCreator::CreateResultImage</a>.  If <a href="https://msdn.microsoft.com/1800717a-3b8a-45b2-849b-55c37d3b1b32">IRawCDImageCreator::put_ResultingImageType</a> is  set to return PQ only, then this call will fail as no RW subcode will be used in the resulting image.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/a83293f6-d5a1-49e2-884b-2b185516109d">IRawCDImageCreator::CreateResultImage</a>



<a href="https://msdn.microsoft.com/1800717a-3b8a-45b2-849b-55c37d3b1b32">IRawCDImageCreator::put_ResultingImageType</a>
 

 


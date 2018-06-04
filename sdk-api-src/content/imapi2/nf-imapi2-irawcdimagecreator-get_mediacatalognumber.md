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

# IRawCDImageCreator::get_MediaCatalogNumber


## -description


Sets the Media Catalog Number (MCN) for the entire audio disc.


## -parameters




### -param value [out]

Pointer to a <b>BSTR</b> value that represents the current MCN associated with the audio disc.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



The MCN returned by this method is formatted as a 13-digit decimal number and must also be provided by  the <a href="https://msdn.microsoft.com/0ba2eaac-3bbc-4625-9c5d-1f1d23bbfa66">IRawCDImageCreator::put_MediaCatalogNumber</a> method  in the same form.  Additionally, the provided a MCN value provided via <b>IRawCDImageCreator::put_MediaCatalogNumber</b>   must have a valid checksum digit (least significant digit), or it will be rejected.  For improved compatibility with scripting, leading zeros may be excluded. For example, "0123456789012" can be expressed as "123456789012".

Please refer to the MMC specification for details regarding the MCN value.  

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/b5fe1a32-545e-417d-9996-34d12862a0ea">IRawCDImageCreator</a>



<a href="https://msdn.microsoft.com/0ba2eaac-3bbc-4625-9c5d-1f1d23bbfa66">IRawCDImageCreator::put_MediaCatalogNumber</a>
 

 


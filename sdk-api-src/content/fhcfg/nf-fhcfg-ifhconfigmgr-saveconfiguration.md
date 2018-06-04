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

# IFhConfigMgr::SaveConfiguration


## -description


Saves to disk all the changes that were made in an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object since the last time that the <a href="https://msdn.microsoft.com/9959AF70-87C2-45E0-A409-959494AF393B">LoadConfiguration</a>, <a href="https://msdn.microsoft.com/70F67D8D-E449-4006-BB14-0E5E9B91D517">CreateDefaultConfiguration</a> or <b>SaveConfiguration</b> method was called  for the File History configuration files of the current user.


## -parameters






## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



This method can be called as many times as needed during the lifetime of an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/70F67D8D-E449-4006-BB14-0E5E9B91D517">IFhConfigMgr::CreateDefaultConfiguration</a>



<a href="https://msdn.microsoft.com/9959AF70-87C2-45E0-A409-959494AF393B">IFhConfigMgr::LoadConfiguration</a>
 

 


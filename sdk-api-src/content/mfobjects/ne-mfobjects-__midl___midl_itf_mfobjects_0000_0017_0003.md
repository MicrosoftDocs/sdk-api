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

# __MIDL___MIDL_itf_mfobjects_0000_0017_0003 enumeration


## -description



          Specifies the behavior when opening a file.
        


## -enum-fields




### -field MF_FILEFLAGS_NONE


            Use the default behavior.
          


### -field MF_FILEFLAGS_NOBUFFERING


            Open the file with no system caching.
          


### -field MF_FILEFLAGS_ALLOW_WRITE_SHARING

Subsequent open operations can have write access to the file.



<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd">MFBeginCreateFile</a>



<a href="https://msdn.microsoft.com/29269ea4-151f-4819-ae49-9f1c13a901e5">MFCreateFile</a>



<a href="https://msdn.microsoft.com/1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678">MFCreateTempFile</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


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

# __MIDL___MIDL_itf_mfobjects_0000_0017_0002 enumeration


## -description



Specifies how to open or create a file.




## -enum-fields




### -field MF_OPENMODE_FAIL_IF_NOT_EXIST

Open an existing file. Fail if the file does not exist.


### -field MF_OPENMODE_FAIL_IF_EXIST

Create a new file. Fail if the file already exists.


### -field MF_OPENMODE_RESET_IF_EXIST

Open an existing file and truncate it, so that the size is zero bytes. Fail if the file does not already exist.


### -field MF_OPENMODE_APPEND_IF_EXIST

If the file does not exist, create a new file. If the file exists, open it.


### -field MF_OPENMODE_DELETE_IF_EXIST

Create a new file. If the file exists, overwrite the file.


## -see-also




<a href="https://msdn.microsoft.com/aca304f6-cf7c-43ea-8ebe-d3bb46f8a2fd">MFBeginCreateFile</a>



<a href="https://msdn.microsoft.com/29269ea4-151f-4819-ae49-9f1c13a901e5">MFCreateFile</a>



<a href="https://msdn.microsoft.com/1f6ce49a-d3f2-4fbe-bbb8-e4ae9bcb0678">MFCreateTempFile</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 


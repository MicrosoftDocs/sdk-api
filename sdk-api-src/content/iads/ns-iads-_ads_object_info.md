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

# _ads_object_info structure


## -description


The <b>ADS_OBJECT_INFO</b> structure specifies the data, including the identity and location, of a directory service object.


## -struct-fields




### -field pszRDN

The null-terminated Unicode string that contains the relative distinguished name of the directory service object.


### -field pszObjectDN

The null-terminated Unicode string that contains the distinguished name  of the directory service object.


### -field pszParentDN

The null-terminated Unicode string that contains the distinguished name of the parent object.


### -field pszSchemaDN

The null-terminated Unicode string that contains the distinguished name of the schema class of the object.


### -field pszClassName

The null-terminated Unicode string that contains the name of the class of which this object is an instance.


## -remarks



To obtain the object data, non-Automation clients call the  <a href="https://msdn.microsoft.com/5a2d7fee-666e-4b3b-b6fa-b9f6d785c2c1">IDirectoryObject::GetObjectInformation</a> method, which takes an out parameter, a pointer to an <b>ADS_OBJECT_INFO</b> structure allocated in the heap. Automation clients can accomplish the same task by calling  <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ee0e469-9932-4135-8798-27d318011786">ADSI Structures</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/5a2d7fee-666e-4b3b-b6fa-b9f6d785c2c1">IDirectoryObject::GetObjectInformation</a>
 

 


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

# BuildTrusteeWithObjectsAndNameW function


## -description



			The <b>BuildTrusteeWithObjectsAndName</b> function initializes a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure with the object-specific <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) information and  initializes the remaining members of the structure to default values. The caller also specifies the name of the trustee.


## -parameters




### -param pTrustee [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure that will be initialized by this function. If the value of this parameter is <b>NULL</b> or a pointer that is not valid, the results are undefined.


### -param pObjName [in, optional]

A pointer to an 
<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a> structure that contains information about the trustee and the securable object.


### -param ObjectType [in, optional]

A pointer to an 
<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a> enumeration that contains information about the type of securable object.


### -param ObjectTypeName [in, optional]

A pointer to a string that specifies the name that corresponds to the ObjectType GUID to be added to the 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure returned in the <i>pTrustee</i> parameter. This function determines the ObjectType GUID that corresponds to this name.


### -param InheritedObjectTypeName [in, optional]

A pointer to a string that specifies the name that corresponds to the InheritedObjectType GUID to be added to the <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure returned in the <i>pTrustee</i> parameter. This function determines the InheritedObjectType GUID that corresponds to this name.


### -param Name [in, optional]

A pointer to a string that specifies the name used to identify the trustee.


## -returns



This function does not return a value.




## -remarks



This function does not allocate memory for the 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> and 
<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a> structures.

For more information about object-specific ACEs, see <a href="https://msdn.microsoft.com/37d353c0-ac22-430f-b5f3-15deb69be24b">Object-specific ACEs</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/a66c23ac-8211-40fd-bfe8-ef9089bf3745">BuildTrusteeWithName</a>



<a href="https://msdn.microsoft.com/e940a87f-013e-458c-bdc1-9e81c7d905e0">BuildTrusteeWithObjectsAndSid</a>



<a href="https://msdn.microsoft.com/3745fbf2-911a-4cb6-81a8-6256c742c700">BuildTrusteeWithSid</a>



<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a>



<a href="https://msdn.microsoft.com/37d353c0-ac22-430f-b5f3-15deb69be24b">Object-specific ACEs</a>



<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 


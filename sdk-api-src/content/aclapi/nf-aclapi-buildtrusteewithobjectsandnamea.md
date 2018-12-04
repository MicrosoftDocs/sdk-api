---
UID: NF:aclapi.BuildTrusteeWithObjectsAndNameA
title: BuildTrusteeWithObjectsAndNameA function
author: windows-sdk-content
description: Initializes a TRUSTEE structure with the object-specific access control entry (ACE) information and initializes the remaining members of the structure to default values. The caller also specifies the name of the trustee.
old-location: security\buildtrusteewithobjectsandname.htm
tech.root: secauthz
ms.assetid: 62edadfe-0a7b-43ec-bd02-a63f928c7618
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: BuildTrusteeWithObjectsAndName, BuildTrusteeWithObjectsAndName function [Security], BuildTrusteeWithObjectsAndNameA, BuildTrusteeWithObjectsAndNameW, _win32_buildtrusteewithobjectsandname, aclapi/BuildTrusteeWithObjectsAndName, aclapi/BuildTrusteeWithObjectsAndNameA, aclapi/BuildTrusteeWithObjectsAndNameW, security.buildtrusteewithobjectsandname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildTrusteeWithObjectsAndNameW (Unicode) and BuildTrusteeWithObjectsAndNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
api_name:
 - BuildTrusteeWithObjectsAndName
 - BuildTrusteeWithObjectsAndNameA
 - BuildTrusteeWithObjectsAndNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# BuildTrusteeWithObjectsAndNameA function


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
 

 


---
UID: NF:aclapi.BuildTrusteeWithObjectsAndSidW
title: BuildTrusteeWithObjectsAndSidW function
author: windows-sdk-content
description: Initializes a TRUSTEE structure with the object-specific access control entry (ACE) information and initializes the remaining members of the structure to default values.
old-location: security\buildtrusteewithobjectsandsid.htm
old-project: SecAuthZ
ms.assetid: e940a87f-013e-458c-bdc1-9e81c7d905e0
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: BuildTrusteeWithObjectsAndSid, BuildTrusteeWithObjectsAndSid function [Security], BuildTrusteeWithObjectsAndSidA, BuildTrusteeWithObjectsAndSidW, _win32_buildtrusteewithobjectsandsid, aclapi/BuildTrusteeWithObjectsAndSid, aclapi/BuildTrusteeWithObjectsAndSidA, aclapi/BuildTrusteeWithObjectsAndSidW, security.buildtrusteewithobjectsandsid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: BuildTrusteeWithObjectsAndSidW (Unicode) and BuildTrusteeWithObjectsAndSidA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TRUSTEE_W, *PTRUSTEE_W, TRUSTEEW, *PTRUSTEEW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-security-trustee-l1-1-0.dll
 - advapi32legacy.dll
 - API-MS-Win-security-trustee-l1-1-1.dll
api_name:
 - BuildTrusteeWithObjectsAndSid
 - BuildTrusteeWithObjectsAndSidA
 - BuildTrusteeWithObjectsAndSidW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# BuildTrusteeWithObjectsAndSidW function


## -description


The <b>BuildTrusteeWithObjectsAndSid</b> function initializes a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure with the object-specific <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) information and initializes the remaining members of the structure to default values. The caller also specifies the 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that represents the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> of the trustee.


## -parameters




### -param pTrustee [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure to initialize. The <b>BuildTrusteeWithObjectsAndSid</b> function does not allocate any memory. If this parameter is <b>NULL</b> or a pointer that is not valid, the results are undefined.


### -param pObjSid [in, optional]

A pointer to an 
<a href="https://msdn.microsoft.com/77ba8a3c-01e5-4a3e-835f-c7b9ef60035a">OBJECTS_AND_SID</a> structure that contains information about the trustee and the securable object.


### -param pObjectGuid [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that describes the ObjectType GUID to be added to the 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


### -param pInheritedObjectGuid [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/323e33b7-676f-4ed0-a9c7-908273c6e10f">GUID</a> structure that describes the InheritedObjectType GUID to be added to the <a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> structure.


### -param pSid [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a> structure that identifies the trustee.


## -returns



This function does not return a value.




## -remarks



This function does not allocate memory for the 
<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a> and 
<a href="https://msdn.microsoft.com/77ba8a3c-01e5-4a3e-835f-c7b9ef60035a">OBJECTS_AND_SID</a> structures.

For more information about object-specific ACEs, see 
<a href="https://msdn.microsoft.com/37d353c0-ac22-430f-b5f3-15deb69be24b">Object-specific ACEs</a>.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/a66c23ac-8211-40fd-bfe8-ef9089bf3745">BuildTrusteeWithName</a>



<a href="https://msdn.microsoft.com/62edadfe-0a7b-43ec-bd02-a63f928c7618">BuildTrusteeWithObjectsAndName</a>



<a href="https://msdn.microsoft.com/3745fbf2-911a-4cb6-81a8-6256c742c700">BuildTrusteeWithSid</a>



<a href="https://msdn.microsoft.com/ad91a302-f693-44e9-9655-ec4488ff78c4">OBJECTS_AND_NAME</a>



<a href="https://msdn.microsoft.com/37d353c0-ac22-430f-b5f3-15deb69be24b">Object-specific ACEs</a>



<a href="https://msdn.microsoft.com/1dee5e3d-0d41-4717-811b-7e05b4deb55f">SE_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/328fba4e-e590-4174-9274-52dad58cb91f">SID</a>



<a href="https://msdn.microsoft.com/120e93eb-680f-4f86-879d-bc2de10d4641">TRUSTEE</a>
 

 


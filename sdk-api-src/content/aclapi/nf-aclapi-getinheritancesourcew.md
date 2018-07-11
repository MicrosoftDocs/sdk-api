---
UID: NF:aclapi.GetInheritanceSourceW
title: GetInheritanceSourceW function
author: windows-sdk-content
description: Returns information about the source of inherited access control entries (ACEs) in an access control list (ACL).
old-location: security\getinheritancesource.htm
old-project: secauthz
ms.assetid: ccc1702b-e414-4831-ae8b-fd92499bec94
ms.author: windowssdkdev
ms.date: 07/04/2018
ms.keywords: GetInheritanceSource, GetInheritanceSource function [Security], GetInheritanceSourceA, GetInheritanceSourceW, _win32_getinheritancesource, aclapi/GetInheritanceSource, aclapi/GetInheritanceSourceA, aclapi/GetInheritanceSourceW, security.getinheritancesource
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetInheritanceSourceW (Unicode) and GetInheritanceSourceA (ANSI)
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
api_name:
 - GetInheritanceSource
 - GetInheritanceSourceA
 - GetInheritanceSourceW
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
---

# GetInheritanceSourceW function


## -description



			The <b>GetInheritanceSource</b> function returns information about the source of inherited <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs) in an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control list</a> (ACL).


## -parameters




### -param pObjectName [in]

A pointer to the name of the object that uses the ACL to be checked.


### -param ObjectType [in]

The type of object indicated by <i>pObjectName</i>. The possible values are SE_FILE_OBJECT, SE_REGISTRY_KEY, SE_DS_OBJECT, and SE_DS_OBJECT_ALL.


### -param SecurityInfo [in]

The type of ACL used with the object. The possible values are DACL_SECURITY_INFORMATION or SACL_SECURITY_INFORMATION.


### -param Container [in]

<b>TRUE</b> if the object is a container object or <b>FALSE</b> if the object is a leaf object. Note that the only leaf object is SE_FILE_OBJECT.


### -param pObjectClassGuids [in, optional]

Optional list of GUIDs that identify the object types or names associated with <i>pObjectName</i>. This may be <b>NULL</b> if the object manager only supports one object class or has no GUID associated with the object class.


### -param GuidCount [in]

Number of GUIDs pointed to by <i>pObjectClassGuids</i>.


### -param pAcl [in]

The ACL for the object.


### -param pfnArray [in, optional]

Reserved. Set this parameter to <b>NULL</b>.


### -param pGenericMapping [in]

The mapping of generic rights to specific rights for the object.


### -param pInheritArray [out]

A pointer to an array of <a href="https://msdn.microsoft.com/6839f67a-6c72-406d-b55e-bc366aaad107">INHERITED_FROM</a> structures that the <b>GetInheritanceSource</b> function fills with the inheritance information. The caller must allocate enough memory for an entry for each ACE in the ACL.


## -returns



 If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.




## -remarks



The <b>GetInheritanceSource</b> function allocates memory for the names returned in the <a href="https://msdn.microsoft.com/6839f67a-6c72-406d-b55e-bc366aaad107">INHERITED_FROM</a> structure. When the function has finished using this memory, the calling program must free it by calling 
<a href="https://msdn.microsoft.com/c9c58b9a-1b65-40e2-b518-30e247f9718e">FreeInheritedFromArray</a>. Note that the caller must provide memory for the array itself. If the caller allocated the memory, the caller must free that memory after calling <b>FreeInheritedFromArray</b>.

This function does not handle race conditions. If your thread calls this function at the approximate time that another thread changes the object's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a>, then this function could fail.




## -see-also




<a href="https://msdn.microsoft.com/c9c58b9a-1b65-40e2-b518-30e247f9718e">FreeInheritedFromArray</a>
 

 


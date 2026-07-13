---
UID: NF:aclapi.GetInheritanceSourceA
title: GetInheritanceSourceA function (aclapi.h)
description: Returns information about the source of inherited access control entries (ACEs) in an access control list (ACL). (ANSI)
helpviewer_keywords: ["GetInheritanceSourceA", "aclapi/GetInheritanceSourceA"]
old-location: security\getinheritancesource.htm
tech.root: security
ms.assetid: ccc1702b-e414-4831-ae8b-fd92499bec94
ms.date: 12/05/2018
ms.keywords: GetInheritanceSource, GetInheritanceSource function [Security], GetInheritanceSourceA, GetInheritanceSourceW, _win32_getinheritancesource, aclapi/GetInheritanceSource, aclapi/GetInheritanceSourceA, aclapi/GetInheritanceSourceW, security.getinheritancesource
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetInheritanceSourceA
 - aclapi/GetInheritanceSourceA
dev_langs:
 - c++
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
---

# GetInheritanceSourceA function


## -description

This version of this function is not supported. The wide character version of this function, [GetInheritanceSourceW](/windows/desktop/api/aclapi/nf-aclapi-getinheritancesourcew), is supported.

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

A pointer to an array of <a href="/windows/desktop/api/accctrl/ns-accctrl-inherited_froma">INHERITED_FROM</a> structures that the <b>GetInheritanceSource</b> function fills with the inheritance information. The caller must allocate enough memory for an entry for each ACE in the ACL.

## -returns

 If the function succeeds, the function returns ERROR_SUCCESS.

If the function fails, it returns a nonzero error code defined in WinError.h.

## -remarks

The <b>GetInheritanceSource</b> function allocates memory for the names returned in the <a href="/windows/desktop/api/accctrl/ns-accctrl-inherited_froma">INHERITED_FROM</a> structure. When the function has finished using this memory, the calling program must free it by calling 
<a href="/windows/desktop/api/aclapi/nf-aclapi-freeinheritedfromarray">FreeInheritedFromArray</a>. Note that the caller must provide memory for the array itself. If the caller allocated the memory, the caller must free that memory after calling <b>FreeInheritedFromArray</b>.

This function does not handle race conditions. If your thread calls this function at the approximate time that another thread changes the object's <a href="/windows/desktop/SecGloss/s-gly">security descriptor</a>, then this function could fail.





> [!NOTE]
> The aclapi.h header defines GetInheritanceSource as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/aclapi/nf-aclapi-freeinheritedfromarray">FreeInheritedFromArray</a>

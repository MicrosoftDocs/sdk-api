---
UID: NF:aclapi.BuildTrusteeWithObjectsAndNameW
title: BuildTrusteeWithObjectsAndNameW function (aclapi.h)
description: Initializes a TRUSTEE structure with the object-specific access control entry (ACE) information and initializes the remaining members of the structure to default values. The caller also specifies the name of the trustee. (Unicode)
helpviewer_keywords: ["BuildTrusteeWithObjectsAndName", "BuildTrusteeWithObjectsAndName function [Security]", "BuildTrusteeWithObjectsAndNameW", "_win32_buildtrusteewithobjectsandname", "aclapi/BuildTrusteeWithObjectsAndName", "aclapi/BuildTrusteeWithObjectsAndNameW", "security.buildtrusteewithobjectsandname"]
old-location: security\buildtrusteewithobjectsandname.htm
tech.root: security
ms.assetid: 62edadfe-0a7b-43ec-bd02-a63f928c7618
ms.date: 12/05/2018
ms.keywords: BuildTrusteeWithObjectsAndName, BuildTrusteeWithObjectsAndName function [Security], BuildTrusteeWithObjectsAndNameA, BuildTrusteeWithObjectsAndNameW, _win32_buildtrusteewithobjectsandname, aclapi/BuildTrusteeWithObjectsAndName, aclapi/BuildTrusteeWithObjectsAndNameA, aclapi/BuildTrusteeWithObjectsAndNameW, security.buildtrusteewithobjectsandname
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BuildTrusteeWithObjectsAndNameW
 - aclapi/BuildTrusteeWithObjectsAndNameW
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
 - BuildTrusteeWithObjectsAndName
 - BuildTrusteeWithObjectsAndNameA
 - BuildTrusteeWithObjectsAndNameW
---

# BuildTrusteeWithObjectsAndNameW function


## -description

The <b>BuildTrusteeWithObjectsAndName</b> function initializes a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure with the object-specific <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) information and  initializes the remaining members of the structure to default values. The caller also specifies the name of the trustee.

## -parameters

### -param pTrustee [in, out]

A pointer to a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure that will be initialized by this function. If the value of this parameter is <b>NULL</b> or a pointer that is not valid, the results are undefined.

### -param pObjName [in, optional]

A pointer to an 
<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a> structure that contains information about the trustee and the securable object.

### -param ObjectType [in, optional]

A pointer to an 
<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a> enumeration that contains information about the type of securable object.

### -param ObjectTypeName [in, optional]

A pointer to a string that specifies the name that corresponds to the ObjectType GUID to be added to the 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure returned in the <i>pTrustee</i> parameter. This function determines the ObjectType GUID that corresponds to this name.

### -param InheritedObjectTypeName [in, optional]

A pointer to a string that specifies the name that corresponds to the InheritedObjectType GUID to be added to the <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure returned in the <i>pTrustee</i> parameter. This function determines the InheritedObjectType GUID that corresponds to this name.

### -param Name [in, optional]

A pointer to a string that specifies the name used to identify the trustee.

## -remarks

This function does not allocate memory for the 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> and 
<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a> structures.

For more information about object-specific ACEs, see <a href="/windows/desktop/SecAuthZ/object-specific-aces">Object-specific ACEs</a>.





> [!NOTE]
> The aclapi.h header defines BuildTrusteeWithObjectsAndName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithnamea">BuildTrusteeWithName</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithobjectsandsida">BuildTrusteeWithObjectsAndSid</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithsida">BuildTrusteeWithSid</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a>



<a href="/windows/desktop/SecAuthZ/object-specific-aces">Object-specific ACEs</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>

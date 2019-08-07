---
UID: NF:aclapi.BuildTrusteeWithObjectsAndSidW
title: BuildTrusteeWithObjectsAndSidW function (aclapi.h)
author: windows-sdk-content
description: Initializes a TRUSTEE structure with the object-specific access control entry (ACE) information and initializes the remaining members of the structure to default values.
old-location: security\buildtrusteewithobjectsandsid.htm
tech.root: SecAuthZ
ms.assetid: e940a87f-013e-458c-bdc1-9e81c7d905e0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: BuildTrusteeWithObjectsAndSid, BuildTrusteeWithObjectsAndSid function [Security], BuildTrusteeWithObjectsAndSidA, BuildTrusteeWithObjectsAndSidW, _win32_buildtrusteewithobjectsandsid, aclapi/BuildTrusteeWithObjectsAndSid, aclapi/BuildTrusteeWithObjectsAndSidA, aclapi/BuildTrusteeWithObjectsAndSidW, security.buildtrusteewithobjectsandsid
ms.topic: function
f1_keywords:
- aclapi/BuildTrusteeWithObjectsAndSid
req.header: aclapi.h
req.include-header: 
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
- API-MS-Win-security-trustee-l1-1-0.dll
- advapi32legacy.dll
- API-MS-Win-security-trustee-l1-1-1.dll
api_name:
- BuildTrusteeWithObjectsAndSid
- BuildTrusteeWithObjectsAndSidA
- BuildTrusteeWithObjectsAndSidW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# BuildTrusteeWithObjectsAndSidW function


## -description


The <b>BuildTrusteeWithObjectsAndSid</b> function initializes a 
<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure with the object-specific <a href="https://docs.microsoft.com/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) information and initializes the remaining members of the structure to default values. The caller also specifies the 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that represents the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> of the trustee.


## -parameters




### -param pTrustee [in, out]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure to initialize. The <b>BuildTrusteeWithObjectsAndSid</b> function does not allocate any memory. If this parameter is <b>NULL</b> or a pointer that is not valid, the results are undefined.


### -param pObjSid [in, optional]

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-objects_and_sid">OBJECTS_AND_SID</a> structure that contains information about the trustee and the securable object.


### -param pObjectGuid [in, optional]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/aa373931(v=vs.80)">GUID</a> structure that describes the ObjectType GUID to be added to the 
<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.


### -param pInheritedObjectGuid [in, optional]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/aa373931(v=vs.80)">GUID</a> structure that describes the InheritedObjectType GUID to be added to the <a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.


### -param pSid [in, optional]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a> structure that identifies the trustee.


## -returns



This function does not return a value.




## -remarks



This function does not allocate memory for the 
<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-objects_and_sid">OBJECTS_AND_SID</a> structures.

For more information about object-specific ACEs, see 
<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/object-specific-aces">Object-specific ACEs</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithnamea">BuildTrusteeWithName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithobjectsandnamea">BuildTrusteeWithObjectsAndName</a>



<a href="https://docs.microsoft.com/windows/desktop/api/aclapi/nf-aclapi-buildtrusteewithsida">BuildTrusteeWithSid</a>



<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-objects_and_name_a">OBJECTS_AND_NAME</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/object-specific-aces">Object-specific ACEs</a>



<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ne-accctrl-se_object_type">SE_OBJECT_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>
 

 


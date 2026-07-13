---
UID: NS:userenv._GROUP_POLICY_OBJECTW
title: GROUP_POLICY_OBJECTW (userenv.h)
description: The GROUP_POLICY_OBJECT structure provides information about a GPO in a GPO list. (Unicode)
helpviewer_keywords: ["*PGROUP_POLICY_OBJECTW","GPLinkDomain","GPLinkMachine","GPLinkOrganizationalUnit","GPLinkSite","GPLinkUnknown","GPO_FLAG_DISABLE","GPO_FLAG_FORCE","GROUP_POLICY_OBJECT","GROUP_POLICY_OBJECT structure [Group Policy]","GROUP_POLICY_OBJECTA","GROUP_POLICY_OBJECTW","PGROUP_POLICY_OBJECT","PGROUP_POLICY_OBJECT structure pointer [Group Policy]","_win32_group_policy_object_str","policy.group_policy_object_str","userenv/GROUP_POLICY_OBJECT","userenv/GROUP_POLICY_OBJECTA","userenv/GROUP_POLICY_OBJECTW","userenv/PGROUP_POLICY_OBJECT"]
old-location: policy\group_policy_object_str.htm
tech.root: Policy
ms.assetid: 7275a3cd-6b19-4eb9-9481-b73bd5af5753
ms.date: 12/05/2018
ms.keywords: '*PGROUP_POLICY_OBJECTW, GPLinkDomain, GPLinkMachine, GPLinkOrganizationalUnit, GPLinkSite, GPLinkUnknown, GPO_FLAG_DISABLE, GPO_FLAG_FORCE, GROUP_POLICY_OBJECT, GROUP_POLICY_OBJECT structure [Group Policy], GROUP_POLICY_OBJECTA, GROUP_POLICY_OBJECTW, PGROUP_POLICY_OBJECT, PGROUP_POLICY_OBJECT structure pointer [Group Policy], _win32_group_policy_object_str, policy.group_policy_object_str, userenv/GROUP_POLICY_OBJECT, userenv/GROUP_POLICY_OBJECTA, userenv/GROUP_POLICY_OBJECTW, userenv/PGROUP_POLICY_OBJECT'
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GROUP_POLICY_OBJECTW (Unicode) and GROUP_POLICY_OBJECTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: GROUP_POLICY_OBJECTW, *PGROUP_POLICY_OBJECTW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _GROUP_POLICY_OBJECTW
 - userenv/_GROUP_POLICY_OBJECTW
 - PGROUP_POLICY_OBJECTW
 - userenv/PGROUP_POLICY_OBJECTW
 - GROUP_POLICY_OBJECTW
 - userenv/GROUP_POLICY_OBJECTW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Userenv.h
api_name:
 - GROUP_POLICY_OBJECT
 - GROUP_POLICY_OBJECTA
 - GROUP_POLICY_OBJECTW
---

# GROUP_POLICY_OBJECTW structure


## -description

The
    <b>GROUP_POLICY_OBJECT</b> structure provides information about a GPO in a GPO list.

## -struct-fields

### -field dwOptions

Specifies link options. This member can be one of the following values.



#### GPO_FLAG_DISABLE

This GPO is disabled.



#### GPO_FLAG_FORCE

Do not override the policy settings in this GPO with policy settings in a subsequent GPO.

### -field dwVersion

Specifies the version number of the GPO.

### -field lpDSPath

Pointer to a string that specifies the path to the directory service portion of the GPO.

### -field lpFileSysPath

Pointer to a string that specifies the path to the file system portion of the GPO.

### -field lpDisplayName

Pointer to the display name of the GPO.

### -field szGPOName

Pointer to a string that specifies a unique name that identifies the GPO.

### -field GPOLink

Specifies the link information for the GPO. This member may be one of the following values.



#### GPLinkUnknown

No link information is available.



#### GPLinkMachine

The GPO is linked to a computer (local or remote).



#### GPLinkSite

The GPO is linked to a site.



#### GPLinkDomain

The GPO is linked to a domain.



#### GPLinkOrganizationalUnit

The GPO is linked to an organizational unit.

### -field lParam

User-supplied data.

### -field pNext

Pointer to the next GPO in the list.

### -field pPrev

Pointer to the previous GPO in the list.

### -field lpExtensions

Extensions that have stored data in this GPO. The format is a string of <b>GUID</b>s grouped in brackets. For more information, see the following Remarks section.

### -field lParam2

User-supplied data.

### -field lpLink

Path to the Active Directory site, domain, or organization unit to which this GPO is linked. If the GPO is linked to the local GPO, this member is "Local".


##### - GPOLink.GPLinkDomain

The GPO is linked to a domain.


##### - GPOLink.GPLinkMachine

The GPO is linked to a computer (local or remote).


##### - GPOLink.GPLinkOrganizationalUnit

The GPO is linked to an organizational unit.


##### - GPOLink.GPLinkSite

The GPO is linked to a site.


##### - GPOLink.GPLinkUnknown

No link information is available.


##### - dwOptions.GPO_FLAG_DISABLE

This GPO is disabled.


##### - dwOptions.GPO_FLAG_FORCE

Do not override the policy settings in this GPO with policy settings in a subsequent GPO.

## -remarks

Each GPO could contain data that must be processed by multiple snap-in extensions. Therefore, the data in the <b>lpExtensions</b> member is organized as a series of <b>GUID</b>s that identify the extensions and snap-in extensions. The data format is as follows:


```cpp
[ext_guid1, snap_in_guid1, snap_in_guid2, ...] 
[ext_guid2, snap_in_guid3, snap_in_guid4, ...] 
```


First, there is an opening bracket, "[", followed by the <b>GUID</b> of the extension. Next, you'll find one or more <b>GUID</b>s identifying the snap-in extensions that have stored data in the GPO. After the last snap-in <b>GUID</b> for an extension, there is a closing bracket, "]". This pattern is repeated for the next extension.





> [!NOTE]
> The userenv.h header defines GROUP_POLICY_OBJECT as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/userenv/nf-userenv-freegpolista">FreeGPOList</a>



<a href="/windows/desktop/api/userenv/nf-userenv-getgpolista">GetGPOList</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-structures">Group Policy Structures</a>

---
UID: NS:objsel._DSOP_UPLEVEL_FILTER_FLAGS
title: DSOP_UPLEVEL_FILTER_FLAGS (objsel.h)
description: The DSOP_UPLEVEL_FILTER_FLAGS structure contains flags that indicate the filters to use for an up-level scope.
helpviewer_keywords: ["DSOP_FILTER_BUILTIN_GROUPS","DSOP_FILTER_COMPUTERS","DSOP_FILTER_CONTACTS","DSOP_FILTER_DOMAIN_LOCAL_GROUPS_DL","DSOP_FILTER_DOMAIN_LOCAL_GROUPS_SE","DSOP_FILTER_GLOBAL_GROUPS_DL","DSOP_FILTER_GLOBAL_GROUPS_SE","DSOP_FILTER_INCLUDE_ADVANCED_VIEW","DSOP_FILTER_PASSWORDSETTINGS_OBJECTS","DSOP_FILTER_SERVICE_ACCOUNTS","DSOP_FILTER_UNIVERSAL_GROUPS_DL","DSOP_FILTER_UNIVERSAL_GROUPS_SE","DSOP_FILTER_USERS","DSOP_FILTER_WELL_KNOWN_PRINCIPALS","DSOP_UPLEVEL_FILTER_FLAGS","DSOP_UPLEVEL_FILTER_FLAGS structure [Active Directory]","_glines_dsop_uplevel_filter_flags","ad.dsop__uplevel__filter__flags","ad.dsop_uplevel_filter_flags","objsel/DSOP_UPLEVEL_FILTER_FLAGS"]
old-location: ad\dsop_uplevel_filter_flags.htm
tech.root: ad
ms.assetid: 54a0046a-7a20-4306-a32f-93e449280574
ms.date: 12/05/2018
ms.keywords: DSOP_FILTER_BUILTIN_GROUPS, DSOP_FILTER_COMPUTERS, DSOP_FILTER_CONTACTS, DSOP_FILTER_DOMAIN_LOCAL_GROUPS_DL, DSOP_FILTER_DOMAIN_LOCAL_GROUPS_SE, DSOP_FILTER_GLOBAL_GROUPS_DL, DSOP_FILTER_GLOBAL_GROUPS_SE, DSOP_FILTER_INCLUDE_ADVANCED_VIEW, DSOP_FILTER_PASSWORDSETTINGS_OBJECTS, DSOP_FILTER_SERVICE_ACCOUNTS, DSOP_FILTER_UNIVERSAL_GROUPS_DL, DSOP_FILTER_UNIVERSAL_GROUPS_SE, DSOP_FILTER_USERS, DSOP_FILTER_WELL_KNOWN_PRINCIPALS, DSOP_UPLEVEL_FILTER_FLAGS, DSOP_UPLEVEL_FILTER_FLAGS structure [Active Directory], _glines_dsop_uplevel_filter_flags, ad.dsop__uplevel__filter__flags, ad.dsop_uplevel_filter_flags, objsel/DSOP_UPLEVEL_FILTER_FLAGS
req.header: objsel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DSOP_UPLEVEL_FILTER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSOP_UPLEVEL_FILTER_FLAGS
 - objsel/_DSOP_UPLEVEL_FILTER_FLAGS
 - DSOP_UPLEVEL_FILTER_FLAGS
 - objsel/DSOP_UPLEVEL_FILTER_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objsel.h
api_name:
 - DSOP_UPLEVEL_FILTER_FLAGS
---

# DSOP_UPLEVEL_FILTER_FLAGS structure


## -description

The <b>DSOP_UPLEVEL_FILTER_FLAGS</b> structure contains flags that indicate the filters to use for an up-level scope. An up-level scope is a scope that supports the ADSI LDAP provider. For more information, see 
<a href="/windows/desktop/ADSI/adsi-ldap-provider">ADSI LDAP Provider</a>. This structure is contained in the <a href="/windows/desktop/api/objsel/ns-objsel-dsop_filter_flags">DSOP_FILTER_FLAGS</a> structure when calling <a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-initialize">IDsObjectPicker::Initialize</a>.

## -struct-fields

### -field flBothModes

Filter flags to use for an up-level scope, regardless of whether it is a mixed or native mode domain. This member can be a combination of one or more of the following flags.



#### DSOP_FILTER_INCLUDE_ADVANCED_VIEW (1 (0x1))

Includes objects that have the <a href="/windows/desktop/ADSchema/a-showinadvancedviewonly">showInAdvancedViewOnly</a> attribute set to <b>TRUE</b>.



#### DSOP_FILTER_USERS (2 (0x2))

Includes <a href="/previous-versions/windows/desktop/winmessenger/im-imsgrsession-user-property">user</a> objects.



#### DSOP_FILTER_BUILTIN_GROUPS (4 (0x4))

Includes built-in <a href="/previous-versions/windows/desktop/axe/group">group</a> objects. Built-in groups are group objects with a <a href="/previous-versions/windows/desktop/mscs/groups-grouptype">groupType</a> value that contain the <b>GROUP_TYPE_BUILTIN_LOCAL_GROUP</b> (0x00000001), <b>GROUP_TYPE_RESOURCE_GROUP</b> (0x00000004), and <b>GROUP_TYPE_SECURITY_ENABLED</b> (0x80000000) flags.



#### DSOP_FILTER_WELL_KNOWN_PRINCIPALS (8 (0x8))

Includes the contents of the Well Known Security Principals container.



#### DSOP_FILTER_UNIVERSAL_GROUPS_DL (16 (0x10))

Includes distribution <a href="/previous-versions/windows/desktop/axe/group">group</a> objects with universal scope.



#### DSOP_FILTER_UNIVERSAL_GROUPS_SE (32 (0x20))

Includes security groups with universal scope. This flag has no effect in a mixed mode domain because universal security groups do not exist in mixed mode domains.



#### DSOP_FILTER_GLOBAL_GROUPS_DL (64 (0x40))

Includes distribution <a href="/previous-versions/windows/desktop/axe/group">group</a> objects with global scope.



#### DSOP_FILTER_GLOBAL_GROUPS_SE (128 (0x80))

Includes security <a href="/previous-versions/windows/desktop/axe/group">group</a> objects with global scope.



#### DSOP_FILTER_DOMAIN_LOCAL_GROUPS_DL (256 (0x100))

Includes distribution <a href="/previous-versions/windows/desktop/axe/group">group</a> objects with domain local scope.



#### DSOP_FILTER_DOMAIN_LOCAL_GROUPS_SE (512 (0x200))

Includes security <a href="/previous-versions/windows/desktop/axe/group">group</a> objects with domain local scope.



#### DSOP_FILTER_CONTACTS (1024 (0x400))

Includes <a href="/previous-versions/windows/desktop/wincontacts/-wincontacts-contact">contact</a> objects.



#### DSOP_FILTER_COMPUTERS (2048 (0x800))

Includes <a href="/windows/desktop/properties/computer-bumper">computer</a> objects.



#### DSOP_FILTER_SERVICE_ACCOUNTS (0x00001000)

Includes managed service account and group managed service account objects.



#### DSOP_FILTER_PASSWORDSETTINGS_OBJECTS (0x00002000)

Includes password settings objects.

### -field flMixedModeOnly

Filter flags to use for an up-level domain in mixed mode. Mixed mode refers to an up-level domain that may have Windows NT 4.0 Backup Domain Controllers present. This member can be a combination of the flags listed in the <b>flBothModes</b> flags. The <b>DSOP_FILTER_UNIVERSAL_GROUPS_SE</b> flag has no effect in a mixed-mode domain because universal security groups do not exist in mixed mode domains.

### -field flNativeModeOnly

Filter flags to use for an up-level domain in native mode. Native mode refers to an up-level domain in which an administrator has enabled native mode operation. This member can be a combination of the flags listed in the <b>flBothModes</b> flags.

## -remarks

For more information about domain modes, see <a href="/windows/desktop/AD/detecting-the-operation-mode-of-a-domain">Detecting the Operation Mode of a Domain</a>.

For more information about group types and scope, see <a href="/windows/desktop/AD/group-objects">Group Objects</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-ldap-provider">ADSI LDAP Provider</a>



<a href="/windows/desktop/api/objsel/ns-objsel-dsop_filter_flags">DSOP_FILTER_FLAGS</a>



<a href="/windows/desktop/AD/directory-object-picker">Directory Object Picker</a>
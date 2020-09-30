---
UID: NS:objsel._DSOP_FILTER_FLAGS
title: DSOP_FILTER_FLAGS (objsel.h)
description: Contains flags that indicate the types of objects presented to the user for a specified scope or scopes.
helpviewer_keywords: ["DSOP_DOWNLEVEL_FILTER_ALL_WELLKNOWN_SIDS","DSOP_DOWNLEVEL_FILTER_ANONYMOUS","DSOP_DOWNLEVEL_FILTER_AUTHENTICATED_USER","DSOP_DOWNLEVEL_FILTER_BATCH","DSOP_DOWNLEVEL_FILTER_COMPUTERS","DSOP_DOWNLEVEL_FILTER_CREATOR_GROUP","DSOP_DOWNLEVEL_FILTER_CREATOR_OWNER","DSOP_DOWNLEVEL_FILTER_DIALUP","DSOP_DOWNLEVEL_FILTER_EXCLUDE_BUILTIN_GROUPS","DSOP_DOWNLEVEL_FILTER_GLOBAL_GROUPS","DSOP_DOWNLEVEL_FILTER_INTERACTIVE","DSOP_DOWNLEVEL_FILTER_INTERNET_USER","DSOP_DOWNLEVEL_FILTER_LOCAL_GROUPS","DSOP_DOWNLEVEL_FILTER_LOCAL_SERVICE","DSOP_DOWNLEVEL_FILTER_NETWORK","DSOP_DOWNLEVEL_FILTER_NETWORK_SERVICE","DSOP_DOWNLEVEL_FILTER_OWNER_RIGHTS","DSOP_DOWNLEVEL_FILTER_REMOTE_LOGON","DSOP_DOWNLEVEL_FILTER_SERVICE","DSOP_DOWNLEVEL_FILTER_SERVICES","DSOP_DOWNLEVEL_FILTER_SYSTEM","DSOP_DOWNLEVEL_FILTER_TERMINAL_SERVER","DSOP_DOWNLEVEL_FILTER_USERS","DSOP_DOWNLEVEL_FILTER_WORLD","DSOP_FILTER_FLAGS","DSOP_FILTER_FLAGS structure [Active Directory]","_glines_dsop_filter_flags","ad.dsop__filter__flags","ad.dsop_filter_flags","objsel/DSOP_FILTER_FLAGS"]
old-location: ad\dsop_filter_flags.htm
tech.root: ad
ms.assetid: 039b2bd8-027e-4b7c-b06b-1ff172c45d52
ms.date: 12/05/2018
ms.keywords: DSOP_DOWNLEVEL_FILTER_ALL_WELLKNOWN_SIDS, DSOP_DOWNLEVEL_FILTER_ANONYMOUS, DSOP_DOWNLEVEL_FILTER_AUTHENTICATED_USER, DSOP_DOWNLEVEL_FILTER_BATCH, DSOP_DOWNLEVEL_FILTER_COMPUTERS, DSOP_DOWNLEVEL_FILTER_CREATOR_GROUP, DSOP_DOWNLEVEL_FILTER_CREATOR_OWNER, DSOP_DOWNLEVEL_FILTER_DIALUP, DSOP_DOWNLEVEL_FILTER_EXCLUDE_BUILTIN_GROUPS, DSOP_DOWNLEVEL_FILTER_GLOBAL_GROUPS, DSOP_DOWNLEVEL_FILTER_INTERACTIVE, DSOP_DOWNLEVEL_FILTER_INTERNET_USER, DSOP_DOWNLEVEL_FILTER_LOCAL_GROUPS, DSOP_DOWNLEVEL_FILTER_LOCAL_SERVICE, DSOP_DOWNLEVEL_FILTER_NETWORK, DSOP_DOWNLEVEL_FILTER_NETWORK_SERVICE, DSOP_DOWNLEVEL_FILTER_OWNER_RIGHTS, DSOP_DOWNLEVEL_FILTER_REMOTE_LOGON, DSOP_DOWNLEVEL_FILTER_SERVICE, DSOP_DOWNLEVEL_FILTER_SERVICES, DSOP_DOWNLEVEL_FILTER_SYSTEM, DSOP_DOWNLEVEL_FILTER_TERMINAL_SERVER, DSOP_DOWNLEVEL_FILTER_USERS, DSOP_DOWNLEVEL_FILTER_WORLD, DSOP_FILTER_FLAGS, DSOP_FILTER_FLAGS structure [Active Directory], _glines_dsop_filter_flags, ad.dsop__filter__flags, ad.dsop_filter_flags, objsel/DSOP_FILTER_FLAGS
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
req.typenames: DSOP_FILTER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DSOP_FILTER_FLAGS
 - objsel/_DSOP_FILTER_FLAGS
 - DSOP_FILTER_FLAGS
 - objsel/DSOP_FILTER_FLAGS
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
 - DSOP_FILTER_FLAGS
---

# DSOP_FILTER_FLAGS structure


## -description

The <b>DSOP_FILTER_FLAGS</b> structure contains flags that indicate the types of objects presented to the user for a specified scope or scopes. This structure is contained in the <a href="/windows/desktop/api/objsel/ns-objsel-dsop_scope_init_info">DSOP_SCOPE_INIT_INFO</a> structure when calling <a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-initialize">IDsObjectPicker::Initialize</a>.

## -struct-fields

### -field Uplevel

Contains a <a href="/windows/desktop/api/objsel/ns-objsel-dsop_uplevel_filter_flags">DSOP_UPLEVEL_FILTER_FLAGS</a> structure that contains the filter flags to use for up-level scopes. An up-level scope is a scope that supports the ADSI LDAP provider. For more information, see 
<a href="/windows/desktop/ADSI/adsi-ldap-provider">ADSI LDAP Provider</a>.

### -field flDownlevel

Contains the filter flags to use for down-level scopes. This member can be a combination of the following flags.



#### DSOP_DOWNLEVEL_FILTER_USERS (0x80000001)

Includes user objects.



#### DSOP_DOWNLEVEL_FILTER_LOCAL_GROUPS (0x80000002)

Includes all local groups.



#### DSOP_DOWNLEVEL_FILTER_GLOBAL_GROUPS (0x80000004)

Includes all global groups.



#### DSOP_DOWNLEVEL_FILTER_COMPUTERS (0x80000008)

Includes computer objects.



#### DSOP_DOWNLEVEL_FILTER_WORLD (0x80000010)

Includes the well-known security principal "World (Everyone)", a group that includes all users.



#### DSOP_DOWNLEVEL_FILTER_AUTHENTICATED_USER (0x80000020)

Includes the well-known security principal "Authenticated User", a group that includes all authenticated accounts in the target domain and its trusted domains.



#### DSOP_DOWNLEVEL_FILTER_ANONYMOUS (0x80000040)

Includes the well-known security principal "Anonymous", which refers to null session logons.



#### DSOP_DOWNLEVEL_FILTER_BATCH (0x80000080)

Includes the well-known security principal "Batch", which refers to batch server logons.



#### DSOP_DOWNLEVEL_FILTER_CREATOR_OWNER (0x80000100)

Includes the well-known security principal "Creator Owner".



#### DSOP_DOWNLEVEL_FILTER_CREATOR_GROUP (0x80000200)

Includes the well-known security principal "Creator Group".



#### DSOP_DOWNLEVEL_FILTER_DIALUP (0x80000400)

Includes the well-known security principal "Dialup".



#### DSOP_DOWNLEVEL_FILTER_INTERACTIVE (0x80000800)

Includes the well-known security principal "Interactive", which refers to users who log on to interactively use the computer.



#### DSOP_DOWNLEVEL_FILTER_NETWORK (0x80001000)

Includes the well-known security principal "Network", which refers to network logons for high performance servers.



#### DSOP_DOWNLEVEL_FILTER_SERVICE (0x80002000)

Includes the well-known security principal "Service", which refers to Win32 service logons.



#### DSOP_DOWNLEVEL_FILTER_SYSTEM (0x80004000)

Includes the well-known security principal "System", which refers to the LocalSystem account.



#### DSOP_DOWNLEVEL_FILTER_EXCLUDE_BUILTIN_GROUPS (0x80008000)

Excludes local built-in groups returned by groups' enumeration.



#### DSOP_DOWNLEVEL_FILTER_TERMINAL_SERVER (0x80010000)

Includes the "Terminal Server" well-known security principal.



#### DSOP_DOWNLEVEL_FILTER_ALL_WELLKNOWN_SIDS (0x80020000)

Includes all well-known security principals. This flag is the same as specifying all of the well-known 
         security principal flags listed in this list.

This flag should be used for forward compatibility because it causes any other down-level, well-known SIDs 
          that might be added in the future your code to automatically be included.



#### DSOP_DOWNLEVEL_FILTER_LOCAL_SERVICE (0x80040000)

Includes the "Local Service" well-known security principal.



#### DSOP_DOWNLEVEL_FILTER_NETWORK_SERVICE (0x80080000)

Includes the "Network Service" well-known security principal.



#### DSOP_DOWNLEVEL_FILTER_REMOTE_LOGON (0x80100000)

Includes the "Remote Logon" well-known security principal.



#### DSOP_DOWNLEVEL_FILTER_INTERNET_USER (0x80200000)

Includes the "Internet User" well-known security principal.



#### DSOP_DOWNLEVEL_FILTER_OWNER_RIGHTS (0x80400000)

Includes the "Owner Rights" well-known security principal.



#### DSOP_DOWNLEVEL_FILTER_SERVICES (0x80800000)

Includes "Service SIDs" of all installed services.

## -see-also

<a href="/windows/desktop/ADSI/adsi-ldap-provider">ADSI LDAP Provider</a>



<a href="/windows/desktop/api/objsel/ns-objsel-dsop_scope_init_info">DSOP_SCOPE_INIT_INFO</a>



<a href="/windows/desktop/api/objsel/ns-objsel-dsop_uplevel_filter_flags">DSOP_UPLEVEL_FILTER_FLAGS</a>



<a href="/windows/desktop/AD/directory-object-picker">Directory Object Picker</a>



<a href="/windows/desktop/api/objsel/nf-objsel-idsobjectpicker-initialize">IDsObjectPicker::Initialize</a>
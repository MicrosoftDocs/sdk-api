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

# _DSOP_FILTER_FLAGS structure


## -description


The <b>DSOP_FILTER_FLAGS</b> structure contains flags that indicate the types of objects presented to the user for a specified scope or scopes. This structure is contained in the <a href="https://msdn.microsoft.com/6262b520-1eee-48e0-b3af-636b66d78b3d">DSOP_SCOPE_INIT_INFO</a> structure when calling <a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a>.


## -struct-fields




### -field Uplevel

Contains a <a href="https://msdn.microsoft.com/54a0046a-7a20-4306-a32f-93e449280574">DSOP_UPLEVEL_FILTER_FLAGS</a> structure that contains the filter flags to use for up-level scopes. An up-level scope is a scope that supports the ADSI LDAP provider. For more information, see 
<a href="https://msdn.microsoft.com/3c13ea2f-fe40-4fd4-8540-422f277e07c1">ADSI LDAP Provider</a>.


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




<a href="https://msdn.microsoft.com/3c13ea2f-fe40-4fd4-8540-422f277e07c1">ADSI LDAP Provider</a>



<a href="https://msdn.microsoft.com/6262b520-1eee-48e0-b3af-636b66d78b3d">DSOP_SCOPE_INIT_INFO</a>



<a href="https://msdn.microsoft.com/54a0046a-7a20-4306-a32f-93e449280574">DSOP_UPLEVEL_FILTER_FLAGS</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a>
 

 


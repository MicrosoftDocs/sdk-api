---
UID: NS:objsel._DSOP_SCOPE_INIT_INFO
title: "_DSOP_SCOPE_INIT_INFO"
author: windows-sdk-content
description: The DSOP_SCOPE_INIT_INFO structure describes one or more scope types that have the same attributes.
old-location: ad\dsop_scope_init_info.htm
old-project: AD
ms.assetid: 6262b520-1eee-48e0-b3af-636b66d78b3d
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PDSOP_SCOPE_INIT_INFO, DSOP_SCOPE_FLAG_DEFAULT_FILTER_COMPUTERS, DSOP_SCOPE_FLAG_DEFAULT_FILTER_CONTACTS, DSOP_SCOPE_FLAG_DEFAULT_FILTER_GROUPS, DSOP_SCOPE_FLAG_DEFAULT_FILTER_PASSWORDSETTINGS_OBJECTS, DSOP_SCOPE_FLAG_DEFAULT_FILTER_SERVICE_ACCOUNTS, DSOP_SCOPE_FLAG_DEFAULT_FILTER_USERS, DSOP_SCOPE_FLAG_STARTING_SCOPE, DSOP_SCOPE_FLAG_WANT_DOWNLEVEL_BUILTIN_PATH, DSOP_SCOPE_FLAG_WANT_PROVIDER_GC, DSOP_SCOPE_FLAG_WANT_PROVIDER_LDAP, DSOP_SCOPE_FLAG_WANT_PROVIDER_WINNT, DSOP_SCOPE_FLAG_WANT_SID_PATH, DSOP_SCOPE_INIT_INFO, DSOP_SCOPE_INIT_INFO structure [Active Directory], DSOP_SCOPE_TYPE_DOWNLEVEL_JOINED_DOMAIN, DSOP_SCOPE_TYPE_ENTERPRISE_DOMAIN, DSOP_SCOPE_TYPE_EXTERNAL_DOWNLEVEL_DOMAIN, DSOP_SCOPE_TYPE_EXTERNAL_UPLEVEL_DOMAIN, DSOP_SCOPE_TYPE_GLOBAL_CATALOG, DSOP_SCOPE_TYPE_TARGET_COMPUTER, DSOP_SCOPE_TYPE_UPLEVEL_JOINED_DOMAIN, DSOP_SCOPE_TYPE_USER_ENTERED_DOWNLEVEL_SCOPE, DSOP_SCOPE_TYPE_USER_ENTERED_UPLEVEL_SCOPE, DSOP_SCOPE_TYPE_WORKGROUP, PCDSOP_SCOPE_INIT_INFO, PCDSOP_SCOPE_INIT_INFO structure pointer [Active Directory], PDSOP_SCOPE_INIT_INFO, PDSOP_SCOPE_INIT_INFO structure pointer [Active Directory], _DSOP_SCOPE_INIT_INFO, _glines_dsop_scope_init_info, ad.dsop__scope__init__info, ad.dsop_scope_init_info, objsel/DSOP_SCOPE_INIT_INFO, objsel/PCDSOP_SCOPE_INIT_INFO, objsel/PDSOP_SCOPE_INIT_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DSOP_SCOPE_INIT_INFO, *PDSOP_SCOPE_INIT_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Objsel.h
api_name:
 - DSOP_SCOPE_INIT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _DSOP_SCOPE_INIT_INFO structure


## -description


The <b>DSOP_SCOPE_INIT_INFO</b> structure describes one or more scope types that have the same attributes. A scope type is a type of location, for example a domain, computer, or Global Catalog, from which the user can select objects.
   This structure is used with  <a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a> when calling <a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a>.


## -struct-fields




### -field cbSize

Contains the size, in bytes, of the structure.


### -field flType

Flags that indicate the scope types described by this structure. You can combine multiple scope types if all specified scopes use the same settings. This member can be a combination of the following flags.



#### DSOP_SCOPE_TYPE_TARGET_COMPUTER (0x00000001)

Computer specified by the <b>pwzTargetComputer</b> member of the 
<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a> structure.

If the target computer is an up-level or down-level domain controller, this flag is ignored unless the <b>DSOP_FLAG_SKIP_TARGET_COMPUTER_DC_CHECK</b>  flag is set in the <b>flOptions</b> member of the <a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a> structure.



#### DSOP_SCOPE_TYPE_UPLEVEL_JOINED_DOMAIN (0x00000002)

An up-level domain to which the target computer is joined. If this flag is set, use the <b>pwzDcName</b> member to specify the name of a domain controller in the joined domain.



#### DSOP_SCOPE_TYPE_DOWNLEVEL_JOINED_DOMAIN (0x00000004)

A down-level domain to which the target computer is joined.



#### DSOP_SCOPE_TYPE_ENTERPRISE_DOMAIN (0x00000008)

All domains in the enterprise to which the target computer belongs. If the <b>DSOP_SCOPE_TYPE_UPLEVEL_JOINED_DOMAIN</b> scope is specified, then the <b>DSOP_SCOPE_TYPE_ENTERPRISE_DOMAIN</b> scope represents all domains in the enterprise except the joined domain.



#### DSOP_SCOPE_TYPE_GLOBAL_CATALOG (0x00000010)

A scope that contains objects from all domains in the enterprise. An enterprise can contain only up-level domains.



#### DSOP_SCOPE_TYPE_EXTERNAL_UPLEVEL_DOMAIN (0x00000020)

All up-level domains external to the enterprise but trusted by the domain to which the target computer is joined.



#### DSOP_SCOPE_TYPE_EXTERNAL_DOWNLEVEL_DOMAIN (0x00000040)

All down-level domains external to the enterprise, but trusted by the domain to which the target computer is joined.



#### DSOP_SCOPE_TYPE_WORKGROUP (0x00000080)

The workgroup to which the target computer is joined. Applies only if the target computer is not joined to a domain. 


The only type of object that can be selected from a workgroup is a computer.



#### DSOP_SCOPE_TYPE_USER_ENTERED_UPLEVEL_SCOPE (0x00000100)

Enables the user to enter an up-level scope. If neither of the <b>DSOP_SCOPE_TYPE_USER_ENTERED_*</b> types is specified, the dialog box restricts the user to the scopes in the <b>Look in</b> drop-down list.



#### DSOP_SCOPE_TYPE_USER_ENTERED_DOWNLEVEL_SCOPE (0x00000200)

Enables the user to enter a down-level scope.


### -field flScope

Flags that indicate the format used to return ADsPath for objects selected from this scope. The <b>flScope</b> member can also indicate the initial scope displayed in the <b>Look in</b> drop-down list. This member can be a combination of the following flags.

LDAP and Global Catalog (GC) paths can be converted to the WinNT ADsPath Syntax. GC paths can be converted to the LDAP format. WinNT objects having an objectSid attribute can be converted to the LDAP format if you specify the <b>DSOP_SCOPE_FLAG_WANT_SID_PATH</b> or <b>DSOP_SCOPE_FLAG_WANT_PROVIDER_LDAP</b> flags. No other conversions are legal.



#### DSOP_SCOPE_FLAG_STARTING_SCOPE (0x00000001)

The scope described by this structure is initially selected in the <b>Look in</b> drop-down list. Only one scope can specify this flag. If no scope specifies this flag, the initial scope is the first successfully created scope in the array of scopes passed to the 
<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a> method.



#### DSOP_SCOPE_FLAG_WANT_PROVIDER_WINNT (0x00000002)

The ADsPaths are converted to use the WinNT provider. For more information, see <a href="https://msdn.microsoft.com/0fad4b34-5287-43a0-a172-a08955b8b132">WinNT ADsPath</a>.



#### DSOP_SCOPE_FLAG_WANT_PROVIDER_LDAP (0x00000004)

The ADsPaths are converted to use the LDAP provider. For more information, see <a href="https://msdn.microsoft.com/adacf6af-8683-4c3c-91bf-9489f2d5d817">LDAP ADsPath</a>.



#### DSOP_SCOPE_FLAG_WANT_PROVIDER_GC (0x00000008)

The ADsPaths for objects selected from this scope are converted to use the GC provider.



#### DSOP_SCOPE_FLAG_WANT_SID_PATH (0x00000010)

The ADsPaths having an <b>objectSid</b> attribute are converted to the form <b>LDAP://&lt;SID=</b><i>x</i><b>&gt;</b> where <i>x</i> represents the hexadecimal digits of the objectSid attribute value.



#### DSOP_SCOPE_FLAG_WANT_DOWNLEVEL_BUILTIN_PATH (0x00000020)

The ADsPaths for down-level, well-known SID objects are an empty string unless this flag is specified (For example; <b>DSOP_DOWNLEVEL_FILTER_INTERACTIVE</b>). If this flag is specified, the paths have the form 


<b>WinNT://NT AUTHORITY/Interactive</b> or <b>WinNT://Creator owner</b>.



#### DSOP_SCOPE_FLAG_DEFAULT_FILTER_USERS (0x00000040)

If the scope filter contains users, select the <b>Users</b> check box in the dialog.



#### DSOP_SCOPE_FLAG_DEFAULT_FILTER_GROUPS (0x00000080)

If the scope filter contains groups, select the <b>Groups</b> check box in the dialog.



#### DSOP_SCOPE_FLAG_DEFAULT_FILTER_COMPUTERS (0x00000100)

If the scope filter contains computers, select the <b>Computers</b> check box in the dialog.



#### DSOP_SCOPE_FLAG_DEFAULT_FILTER_CONTACTS (0x00000200)

If the scope filter contains contacts, select the <b>Contacts</b> check box in the dialog.



#### DSOP_SCOPE_FLAG_DEFAULT_FILTER_SERVICE_ACCOUNTS (0x00000400)

If the scope filter contains service accounts, select the <b>Service Accounts</b> and <b>Group Managed Service Accounts</b> check boxes in the dialog.



#### DSOP_SCOPE_FLAG_DEFAULT_FILTER_PASSWORDSETTINGS_OBJECTS (0x00000800)

If the scope filter contains password setting objects, select the <b>Password Setting Objects</b> check box in the dialog.


### -field FilterFlags

Contains a <a href="https://msdn.microsoft.com/039b2bd8-027e-4b7c-b06b-1ff172c45d52">DSOP_FILTER_FLAGS</a> structure that indicates the types of objects presented to the user for this scope or scopes.


### -field pwzDcName

Pointer to a null-terminated Unicode string that contains the name of a domain controller of the domain to which the target computer is joined. This member is used only if the <b>flType</b> member contains the <b>DSOP_SCOPE_TYPE_UPLEVEL_JOINED_DOMAIN</b> flag. If that flag is not set, <b>pwzDcName</b> must be <b>NULL</b>.

This member can be <b>NULL</b> even if the <b>DSOP_SCOPE_TYPE_UPLEVEL_JOINED_DOMAIN</b> flag is specified, in which case, the dialog box looks up the domain controller. This member enables you to name a specific domain controller in a multimaster domain. For example, an administrative application might make changes on a domain controller in a multimaster domain, and then open the object picker dialog box before the changes have been replicated on the other domain controllers.


### -field pwzADsPath

Reserved; must be <b>NULL</b>.


### -field hr

Contains an <b>HRESULT</b> value that indicates the status of the specific scope. If the 
<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a> method successfully creates the scope, or scopes, specified by this structure, <b>hr</b> contains <b>S_OK</b>. Otherwise, <b>hr</b> contains an error code.

If <a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a> returns <b>S_OK</b>, the <b>hr</b> members of all the specified <b>DSOP_SCOPE_INIT_INFO</b> structures also contain <b>S_OK</b>.


## -see-also




<a href="https://msdn.microsoft.com/039b2bd8-027e-4b7c-b06b-1ff172c45d52">DSOP_FILTER_FLAGS</a>



<a href="https://msdn.microsoft.com/6d070185-e0b6-4c24-9941-95bca2f33192">DSOP_INIT_INFO</a>



<a href="https://msdn.microsoft.com/5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a">Directory Object Picker</a>



<a href="https://msdn.microsoft.com/bcf4d283-6709-4425-a122-8f0808502b58">IDsObjectPicker::Initialize</a>
 

 


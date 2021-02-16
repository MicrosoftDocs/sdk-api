---
UID: NS:authz._AUTHZ_SOURCE_SCHEMA_REGISTRATION
title: AUTHZ_SOURCE_SCHEMA_REGISTRATION (authz.h)
description: Specifies information about source schema registration.
helpviewer_keywords: ["*PAUTHZ_SOURCE_SCHEMA_REGISTRATION","AUTHZ_ALLOW_MULTIPLE_SOURCE_INSTANCES","AUTHZ_MIGRATED_LEGACY_PUBLISHER","AUTHZ_SOURCE_SCHEMA_REGISTRATION","AUTHZ_SOURCE_SCHEMA_REGISTRATION structure [Security]","PAUTHZ_SOURCE_SCHEMA_REGISTRATION","PAUTHZ_SOURCE_SCHEMA_REGISTRATION structure pointer [Security]","authz/AUTHZ_SOURCE_SCHEMA_REGISTRATION","authz/PAUTHZ_SOURCE_SCHEMA_REGISTRATION","security.authz_source_schema_registration"]
old-location: security\authz_source_schema_registration.htm
tech.root: security
ms.assetid: 8b4d6e14-fb9c-428a-bd94-34eba668edc6
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_SOURCE_SCHEMA_REGISTRATION, AUTHZ_ALLOW_MULTIPLE_SOURCE_INSTANCES, AUTHZ_MIGRATED_LEGACY_PUBLISHER, AUTHZ_SOURCE_SCHEMA_REGISTRATION, AUTHZ_SOURCE_SCHEMA_REGISTRATION structure [Security], PAUTHZ_SOURCE_SCHEMA_REGISTRATION, PAUTHZ_SOURCE_SCHEMA_REGISTRATION structure pointer [Security], authz/AUTHZ_SOURCE_SCHEMA_REGISTRATION, authz/PAUTHZ_SOURCE_SCHEMA_REGISTRATION, security.authz_source_schema_registration'
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AUTHZ_SOURCE_SCHEMA_REGISTRATION, *PAUTHZ_SOURCE_SCHEMA_REGISTRATION
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_SOURCE_SCHEMA_REGISTRATION
 - authz/_AUTHZ_SOURCE_SCHEMA_REGISTRATION
 - PAUTHZ_SOURCE_SCHEMA_REGISTRATION
 - authz/PAUTHZ_SOURCE_SCHEMA_REGISTRATION
 - AUTHZ_SOURCE_SCHEMA_REGISTRATION
 - authz/AUTHZ_SOURCE_SCHEMA_REGISTRATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_SOURCE_SCHEMA_REGISTRATION
---

# AUTHZ_SOURCE_SCHEMA_REGISTRATION structure


## -description

The <b>AUTHZ_SOURCE_SCHEMA_REGISTRATION</b> structure specifies information about source schema registration.

## -struct-fields

### -field dwFlags

Flags that control the behavior of the operation. The following table shows a possible value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_ALLOW_MULTIPLE_SOURCE_INSTANCES"></a><a id="authz_allow_multiple_source_instances"></a><dl>
<dt><b>AUTHZ_ALLOW_MULTIPLE_SOURCE_INSTANCES</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Allows registration of  multiple sources with the same name.  Use of this flag  means that   more than one source can call the <a href="/windows/desktop/api/authz/nf-authz-authzregistersecurityeventsource">AuthzRegisterSecurityEventSource</a> function with the same <i>szEventSourceName</i> at runtime.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_MIGRATED_LEGACY_PUBLISHER"></a><a id="authz_migrated_legacy_publisher"></a><dl>
<dt><b>AUTHZ_MIGRATED_LEGACY_PUBLISHER</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The caller is a migrated publisher that has registered a manifest with WEvtUtil.exe. The <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> of the provider specified by the <b>pProviderGuid</b> member is stored in the registry.

</td>
</tr>
</table>

### -field szEventSourceName

A pointer to a wide character string that represents the name of the event source.

### -field szEventMessageFile

A pointer to a wide character string that represents the name of the resource that contains the event messages.

### -field szEventSourceXmlSchemaFile

A pointer to a wide character string that represents the name of the XML schema file for the event source.

### -field szEventAccessStringsFile

A pointer to a wide character string that represents the name of the resource that contains the event parameter strings.

### -field szExecutableImagePath

This member is reserved and must be set to <b>NULL</b>.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pReserved

This member is reserved and must be set to <b>NULL</b>.

### -field DUMMYUNIONNAME.pProviderGuid

The <a href="/windows/win32/api/guiddef/ns-guiddef-guid">GUID</a> of a migrated publisher. The value of this member is converted to a string and stored in the registry if the caller is a migrated publisher.

### -field dwObjectTypeNameCount

The number of objects in the <i>ObjectTypeNames</i> array.

### -field ObjectTypeNames

An array of <a href="/windows/win32/api/authz/ns-authz-authz_registration_object_type_name_offset">AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET</a> structures that represents the object types for the events.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzenumeratesecurityeventsources">AuthzEnumerateSecurityEventSources</a>



<a href="/windows/desktop/api/authz/nf-authz-authzinstallsecurityeventsource">AuthzInstallSecurityEventSource</a>
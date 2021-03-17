---
UID: NS:winnt._CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
title: CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1 (winnt.h)
description: Defines a resource attribute that is defined in continuous memory for persistence within a serialized security descriptor.
helpviewer_keywords: ["*PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1","CLAIM_SECURITY_ATTRIBUTE_DISABLED","CLAIM_SECURITY_ATTRIBUTE_DISABLED_BY_DEFAULT","CLAIM_SECURITY_ATTRIBUTE_MANDATORY","CLAIM_SECURITY_ATTRIBUTE_NON_INHERITABLE","CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1","CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1 structure [Security]","CLAIM_SECURITY_ATTRIBUTE_TYPE_INT64","CLAIM_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING","CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING","CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64","CLAIM_SECURITY_ATTRIBUTE_USE_FOR_DENY_ONLY","CLAIM_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE","PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1","PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1 structure pointer [Security]","_CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1","security.claim_security_attribute_relative_v1","winnt/CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1","winnt/PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1"]
old-location: security\claim_security_attribute_relative_v1.htm
tech.root: security
ms.assetid: 7516CFA6-3726-4004-854E-CD07347898E5
ms.date: 12/05/2018
ms.keywords: '*PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1, CLAIM_SECURITY_ATTRIBUTE_DISABLED, CLAIM_SECURITY_ATTRIBUTE_DISABLED_BY_DEFAULT, CLAIM_SECURITY_ATTRIBUTE_MANDATORY, CLAIM_SECURITY_ATTRIBUTE_NON_INHERITABLE, CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1, CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1 structure [Security], CLAIM_SECURITY_ATTRIBUTE_TYPE_INT64, CLAIM_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING, CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING, CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64, CLAIM_SECURITY_ATTRIBUTE_USE_FOR_DENY_ONLY, CLAIM_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE, PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1, PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1 structure pointer [Security], _CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1, security.claim_security_attribute_relative_v1, winnt/CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1, winnt/PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1, *PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
 - winnt/_CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
 - PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
 - winnt/PCLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
 - CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
 - winnt/CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1
---

# CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1 structure


## -description

The <b>CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1</b> structure defines a resource attribute that is defined in continuous memory for persistence within a serialized security descriptor.

## -struct-fields

### -field Name

A value that indicates an offset from the beginning of the <b>CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1</b> structure to a string of Unicode characters that contain the name of the claim security attribute. The string must be at least 4 bytes in length.

### -field ValueType

A union tag value that indicates the type of information being referred to by the <b>Values</b> member. The <b>Values</b> member will contain an array of offsets from the beginning of the <b>CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1</b> structure to each value. The <b>ValueType</b> member must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_INT64"></a><a id="claim_security_attribute_type_int64"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_INT64</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of offsets to <b>LONG64</b> values.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64"></a><a id="claim_security_attribute_type_uint64"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of offsets to <b>ULONG64</b> values.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING"></a><a id="claim_security_attribute_type_string"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of offsets to Unicode character string values.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING"></a><a id="claim_security_attribute_type_octet_string"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of <a href="/windows/win32/api/winnt/ns-winnt-claim_security_attribute_octet_string_value">CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</a> values.

</td>
</tr>
</table>

### -field Reserved

This member is currently reserved and must be set to zero when sent and must be ignored when received.

### -field Flags

The claim security attribute flags must be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_NON_INHERITABLE"></a><a id="claim_security_attribute_non_inheritable"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_NON_INHERITABLE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
This claim security attribute is  not inherited across processes.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE"></a><a id="claim_security_attribute_value_case_sensitive"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The value of the claim security attribute is case sensitive. This flag is valid for values that contain string types.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_USE_FOR_DENY_ONLY"></a><a id="claim_security_attribute_use_for_deny_only"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_USE_FOR_DENY_ONLY</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The claim security attribute is considered only for deny <a href="/windows/desktop/SecGloss/a-gly">access control entries</a> (ACEs).

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_DISABLED_BY_DEFAULT"></a><a id="claim_security_attribute_disabled_by_default"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_DISABLED_BY_DEFAULT</b></dt>
<dt>0x0008</dt>
</dl>
</td>
<td width="60%">
The claim security attribute is disabled by default.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_DISABLED"></a><a id="claim_security_attribute_disabled"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_DISABLED</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The claim security attribute is disabled.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_MANDATORY"></a><a id="claim_security_attribute_mandatory"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_MANDATORY</b></dt>
<dt>0x0020</dt>
</dl>
</td>
<td width="60%">
The claim security attribute is mandatory.

</td>
</tr>
</table>

### -field ValueCount

The number of values contained in the <b>Values</b> member.

### -field Values

An array of offsets from the beginning of the CLAIM_SECURITY_ATTRIBUTE_RELATIVE_V1 structure. Each offset indicates the location of a claim security attribute value of the type specified in the <b>ValueType</b> member.

### -field Values.pInt64

Pointer to an array of <b>ValueCount</b> members that is an offset from the beginning of the structure to a <b>LONG64</b> of type CLAIM_SECURITY_ATTRIBUTE_TYPE_INT64.

### -field Values.pUint64

Pointer to an array of <b>ValueCount</b> members where each member is an offset from the beginning of the structure to a <b>ULONG64</b>  of type CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64.

### -field Values.ppString

Pointer to an array of <b>ValueCount</b> members where each member is an offset from the beginning of the structure to a <b>PWSTR</b>  of type CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING.

### -field Values.pFqbn

Pointer to an array of <b>ValueCount</b> members where each member is an offset from the beginning of the structure to the fully qualified binary name value of type <a href="/windows/desktop/api/winnt/ns-winnt-claim_security_attribute_fqbn_value">CLAIM_SECURITY_ATTRIBUTE_FQBN_VALUE</a>.

### -field Values.pOctetString

Pointer to an array of <b>ValueCount</b> members where each member is an offset from the beginning of the structure to a <b>LONG64</b> octet string of type <a href="/windows/win32/api/winnt/ns-winnt-claim_security_attribute_octet_string_value">CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</a>.
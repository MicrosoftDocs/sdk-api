---
UID: NS:winnt._CLAIM_SECURITY_ATTRIBUTE_V1
title: "_CLAIM_SECURITY_ATTRIBUTE_V1"
author: windows-sdk-content
description: Defines a security attribute that can be associated with a token or authorization context.
old-location: security\claim_security_attribute_v1.htm
old-project: secauthz
ms.assetid: FDBB9B00-01C3-474A-81FF-97C5CBA3261B
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*PCLAIM_SECURITY_ATTRIBUTE_V1, CLAIM_SECURITY_ATTRIBUTE_DISABLED, CLAIM_SECURITY_ATTRIBUTE_DISABLED_BY_DEFAULT, CLAIM_SECURITY_ATTRIBUTE_MANDATORY, CLAIM_SECURITY_ATTRIBUTE_NON_INHERITABLE, CLAIM_SECURITY_ATTRIBUTE_TYPE_BOOLEAN, CLAIM_SECURITY_ATTRIBUTE_TYPE_FQBN, CLAIM_SECURITY_ATTRIBUTE_TYPE_INT64, CLAIM_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING, CLAIM_SECURITY_ATTRIBUTE_TYPE_SID, CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING, CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64, CLAIM_SECURITY_ATTRIBUTE_USE_FOR_DENY_ONLY, CLAIM_SECURITY_ATTRIBUTE_V1, CLAIM_SECURITY_ATTRIBUTE_V1 structure [Security], CLAIM_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE, PCLAIM_SECURITY_ATTRIBUTE_V1, PCLAIM_SECURITY_ATTRIBUTE_V1 structure pointer [Security], _CLAIM_SECURITY_ATTRIBUTE_V1, security.claim_security_attribute_v1, winnt/CLAIM_SECURITY_ATTRIBUTE_V1, winnt/PCLAIM_SECURITY_ATTRIBUTE_V1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: CLAIM_SECURITY_ATTRIBUTE_V1, *PCLAIM_SECURITY_ATTRIBUTE_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - CLAIM_SECURITY_ATTRIBUTE_V1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _CLAIM_SECURITY_ATTRIBUTE_V1 structure


## -description


The <b>CLAIM_SECURITY_ATTRIBUTE_V1</b> structure defines a security attribute that can be associated with a token or authorization context.


## -struct-fields




### -field Name

A pointer to a string of Unicode characters that contains the name of the security attribute. This string must be at least 4 bytes in length.


### -field ValueType

A union tag value that indicates the type of information contained in the <b>Values</b> member. The <b>ValueType</b> member must be one of the following values.

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
The <b>Values</b> member refers to an array of <b>LONG64</b> values.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64"></a><a id="claim_security_attribute_type_uint64"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of <b>ULONG64</b> values.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING"></a><a id="claim_security_attribute_type_string"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of pointers to Unicode string values.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_FQBN"></a><a id="claim_security_attribute_type_fqbn"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_FQBN</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of <a href="https://msdn.microsoft.com/1FD9A519-40EA-4780-90F5-C9DF4ADAE72C">CLAIM_SECURITY_ATTRIBUTE_FQBN_VALUE</a> values.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_SID"></a><a id="claim_security_attribute_type_sid"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_SID</b></dt>
<dt>0x0005</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of <a href="https://msdn.microsoft.com/6647CC4F-1A84-43B2-A80E-7B6BF3A2D7AD">CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</a> values where the <b>pValue</b> member of each <b>CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</b> is a <b>PSID</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_BOOLEAN"></a><a id="claim_security_attribute_type_boolean"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_BOOLEAN</b></dt>
<dt>0x0006</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of <b>ULONG64</b> values where each element indicates a Boolean value. The value 1 indicates <b>TRUE</b> and the value 0 indicates <b>FALSE</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CLAIM_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING"></a><a id="claim_security_attribute_type_octet_string"></a><dl>
<dt><b>CLAIM_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to an array of <a href="https://msdn.microsoft.com/6647CC4F-1A84-43B2-A80E-7B6BF3A2D7AD">CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</a> values.

</td>
</tr>
</table>
 


### -field Reserved

This member is reserved and must be set to zero when sent and must be ignored when received.


### -field Flags

The attribute flags that are a 32-bitmask. Bits 16 through 31 may be set to any value. Bits 0 through 15 must be zero or a combination of one or more of the following mask values.

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
This attribute is ignored by the operating system. This claim security attribute is not inherited across processes.

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
The claim security attribute is considered only for deny <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entries</a> (ACEs).

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
The claim security attribute is disabled and will not be applied by the <a href="https://msdn.microsoft.com/d9fd2e44-5782-40c9-a1cf-1788ca7afc50">AccessCheck</a> function.

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

The number of values specified in the <b>Values</b> member.


### -field Values

An array of security attribute values of the type specified in the <b>ValueType</b> member.


### -field Values.pInt64

Pointer to an array of <b>ValueCount</b> members where each member is  a <b>LONG64</b> of type CLAIM_SECURITY_ATTRIBUTE_TYPE_INT64.


### -field Values.pUint64

Pointer to an array of <b>ValueCount</b> members where each member is  a <b>ULONG64</b>  of type CLAIM_SECURITY_ATTRIBUTE_TYPE_UINT64.


### -field Values.ppString

Pointer to an array of <b>ValueCount</b> members where each member is  a <b>PWSTR</b>  of type CLAIM_SECURITY_ATTRIBUTE_TYPE_STRING.


### -field Values.pFqbn

Pointer to an array of <b>ValueCount</b> members where each member is a fully qualified binary name value of type <a href="https://msdn.microsoft.com/1FD9A519-40EA-4780-90F5-C9DF4ADAE72C">CLAIM_SECURITY_ATTRIBUTE_FQBN_VALUE</a>.


### -field Values.pOctetString

Pointer to an array of <b>ValueCount</b> members where each member is  an octet string of type <a href="https://msdn.microsoft.com/6647CC4F-1A84-43B2-A80E-7B6BF3A2D7AD">CLAIM_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</a>.


## -see-also




<a href="https://msdn.microsoft.com/D7D9816E-1ECE-48CA-9F2F-0955572A0FCA">CLAIM_SECURITY_ATTRIBUTES_INFORMATION</a>
 

 


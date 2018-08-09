---
UID: NS:authz._AUTHZ_SECURITY_ATTRIBUTE_V1
title: "_AUTHZ_SECURITY_ATTRIBUTE_V1"
author: windows-sdk-content
description: Defines a security attribute that can be associated with an authorization context.
old-location: security\authz_security_attribute_v1.htm
old-project: secauthz
ms.assetid: 0c4778bb-1b5d-4422-b066-d2a6aaa1f351
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PAUTHZ_SECURITY_ATTRIBUTE_V1, AUTHZ_SECURITY_ATTRIBUTE_NON_INHERITABLE, AUTHZ_SECURITY_ATTRIBUTE_TYPE_BOOLEAN, AUTHZ_SECURITY_ATTRIBUTE_TYPE_FQBN, AUTHZ_SECURITY_ATTRIBUTE_TYPE_INT64, AUTHZ_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING, AUTHZ_SECURITY_ATTRIBUTE_TYPE_SID, AUTHZ_SECURITY_ATTRIBUTE_TYPE_STRING, AUTHZ_SECURITY_ATTRIBUTE_TYPE_UINT64, AUTHZ_SECURITY_ATTRIBUTE_V1, AUTHZ_SECURITY_ATTRIBUTE_V1 structure [Security], AUTHZ_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE, PAUTHZ_SECURITY_ATTRIBUTE_V1, PAUTHZ_SECURITY_ATTRIBUTE_V1 structure pointer [Security], _AUTHZ_SECURITY_ATTRIBUTE_V1, authz/AUTHZ_SECURITY_ATTRIBUTE_V1, authz/PAUTHZ_SECURITY_ATTRIBUTE_V1, security.authz_security_attribute_v1"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: AUTHZ_SECURITY_ATTRIBUTE_V1, *PAUTHZ_SECURITY_ATTRIBUTE_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_SECURITY_ATTRIBUTE_V1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _AUTHZ_SECURITY_ATTRIBUTE_V1 structure


## -description


The <b>AUTHZ_SECURITY_ATTRIBUTE_V1</b> structure defines a security attribute that can be associated with an authorization context.


## -struct-fields




### -field pName

A pointer to a name of a security attribute.


### -field ValueType

The data type of the values pointed to by the <b>Values</b> member.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_INT64"></a><a id="authz_security_attribute_type_int64"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_INT64</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>INT64</b> type.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_UINT64"></a><a id="authz_security_attribute_type_uint64"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_UINT64</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>UINT64</b> type.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_STRING"></a><a id="authz_security_attribute_type_string"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_STRING</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>STRING</b> type.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_FQBN"></a><a id="authz_security_attribute_type_fqbn"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_FQBN</b></dt>
<dt>0x0004</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_FQBN</b> type.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_SID"></a><a id="authz_security_attribute_type_sid"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_SID</b></dt>
<dt>0x0005</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_SID</b> type.

<b>Windows Server 2008 R2 and Windows 7:  </b>This value type is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_BOOLEAN"></a><a id="authz_security_attribute_type_boolean"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_BOOLEAN</b></dt>
<dt>0x0006</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_BOOLEAN</b> type.

<b>Windows Server 2008 R2 and Windows 7:  </b>This value type is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING"></a><a id="authz_security_attribute_type_octet_string"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING</b> type.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING"></a><a id="authz_security_attribute_type_octet_string"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING</b></dt>
<dt>0x0010</dt>
</dl>
</td>
<td width="60%">
The <b>Values</b> member refers to a security attribute that is of <b>AUTHZ_SECURITY_ATTRIBUTE_TYPE_OCTET_STRING</b> type.

</td>
</tr>
</table>
 


### -field Reserved

Reserved for future use.


### -field Flags

A combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_NON_INHERITABLE"></a><a id="authz_security_attribute_non_inheritable"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_NON_INHERITABLE</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
This security attribute is not inherited across processes.

</td>
</tr>
<tr>
<td width="40%"><a id="AUTHZ_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE"></a><a id="authz_security_attribute_value_case_sensitive"></a><dl>
<dt><b>AUTHZ_SECURITY_ATTRIBUTE_VALUE_CASE_SENSITIVE</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The value of the attribute is case sensitive. This flag is valid for values that contain string types.

</td>
</tr>
</table>
 


### -field ValueCount

The number of values specified in the <b>Values</b> member.


### -field Values


### -field Values.pInt64

A pointer to one or more numeric attribute values.


### -field Values.pUint64

A pointer to one or more numeric attribute values.


### -field Values.ppString

A pointer to one or more string attribute values.


### -field Values.pFqbn

A pointer to one or more <a href="https://msdn.microsoft.com/05b4bf7d-a0d9-473c-b215-9cf566b2a996">AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE</a> structures.


### -field Values.pOctetString

A pointer to one or more <a href="https://msdn.microsoft.com/aebe20d5-280f-45d3-a11d-279a08a1a165">AUTHZ_SECURITY_ATTRIBUTE_OCTET_STRING_VALUE</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</a>



<a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a>
 

 


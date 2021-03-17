---
UID: NS:winnt._SYSTEM_MANDATORY_LABEL_ACE
title: SYSTEM_MANDATORY_LABEL_ACE (winnt.h)
description: Defines an access control entry (ACE) for the system access control list (SACL) that specifies the mandatory access level and policy for a securable object.
helpviewer_keywords: ["*PSYSTEM_MANDATORY_LABEL_ACE","PSYSTEM_MANDATORY_LABEL_ACE","PSYSTEM_MANDATORY_LABEL_ACE structure pointer [Security]","SYSTEM_MANDATORY_LABEL_ACE","SYSTEM_MANDATORY_LABEL_ACE structure [Security]","SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP","SYSTEM_MANDATORY_LABEL_NO_READ_UP","SYSTEM_MANDATORY_LABEL_NO_WRITE_UP","_SYSTEM_MANDATORY_LABEL_ACE","security.system_mandatory_label_ace","winnt/PSYSTEM_MANDATORY_LABEL_ACE","winnt/SYSTEM_MANDATORY_LABEL_ACE"]
old-location: security\system_mandatory_label_ace.htm
tech.root: security
ms.assetid: 77b7716c-b445-4473-a2e3-4a78f9fbebe3
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_MANDATORY_LABEL_ACE, PSYSTEM_MANDATORY_LABEL_ACE, PSYSTEM_MANDATORY_LABEL_ACE structure pointer [Security], SYSTEM_MANDATORY_LABEL_ACE, SYSTEM_MANDATORY_LABEL_ACE structure [Security], SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP, SYSTEM_MANDATORY_LABEL_NO_READ_UP, SYSTEM_MANDATORY_LABEL_NO_WRITE_UP, _SYSTEM_MANDATORY_LABEL_ACE, security.system_mandatory_label_ace, winnt/PSYSTEM_MANDATORY_LABEL_ACE, winnt/SYSTEM_MANDATORY_LABEL_ACE'
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SYSTEM_MANDATORY_LABEL_ACE, *PSYSTEM_MANDATORY_LABEL_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_MANDATORY_LABEL_ACE
 - winnt/_SYSTEM_MANDATORY_LABEL_ACE
 - PSYSTEM_MANDATORY_LABEL_ACE
 - winnt/PSYSTEM_MANDATORY_LABEL_ACE
 - SYSTEM_MANDATORY_LABEL_ACE
 - winnt/SYSTEM_MANDATORY_LABEL_ACE
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
 - SYSTEM_MANDATORY_LABEL_ACE
---

# SYSTEM_MANDATORY_LABEL_ACE structure


## -description

The <b>SYSTEM_MANDATORY_LABEL_ACE</b> structure defines an  <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) for the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) that specifies the mandatory access level and policy for a securable object.

## -struct-fields

### -field Header

An <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of the ACE. The structure also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure must be set to <b>SYSTEM_MANDATORY_LABEL_ACE_TYPE</b>, and the <b>AceSize</b> member must be set to the total number of bytes allocated for the <b>SYSTEM_MANDATORY_LABEL_ACE</b> structure.

### -field Mask

The access policy for principals with a mandatory integrity level lower than the object associated with the SACL that contains this ACE.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_NO_WRITE_UP"></a><a id="system_mandatory_label_no_write_up"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_NO_WRITE_UP</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
A principal with a lower mandatory level than the object cannot write to the object.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_NO_READ_UP"></a><a id="system_mandatory_label_no_read_up"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_NO_READ_UP</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
A principal with a lower mandatory level than the object cannot read the object.

</td>
</tr>
<tr>
<td width="40%"><a id="SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP"></a><a id="system_mandatory_label_no_execute_up"></a><dl>
<dt><b>SYSTEM_MANDATORY_LABEL_NO_EXECUTE_UP</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
A principal with a lower mandatory level than the object cannot execute the object.

</td>
</tr>
</table>

### -field SidStart

Specifies the first <b>DWORD</b> of a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>. The remaining bytes of the <b>SID</b>  are stored in contiguous memory after the <b>SidStart</b> member. The identifier authority of the <b>SID</b> must be <b>SECURITY_MANDATORY_LABEL_AUTHORITY</b>. The <a href="/windows/desktop/SecGloss/r-gly">RID</a> of the <b>SID</b> specifies the mandatory integrity level of the object associated with the SACL that contains this ACE. The <i>RID</i> must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1000</dt>
</dl>
</td>
<td width="60%">
Low integrity level.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x2000</dt>
</dl>
</td>
<td width="60%">
Medium integrity level.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x3000</dt>
</dl>
</td>
<td width="60%">
High integrity level.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-acl">ACL</a>
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

# _SYSTEM_MANDATORY_LABEL_ACE structure


## -description


The <b>SYSTEM_MANDATORY_LABEL_ACE</b> structure defines an  <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access control entry</a> (ACE) for the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL) that specifies the mandatory access level and policy for a securable object.


## -struct-fields




### -field Header

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff538847">ACE_HEADER</a> structure that specifies the size and type of the ACE. The structure also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure must be set to <b>SYSTEM_MANDATORY_LABEL_ACE_TYPE</b>, and the <b>AceSize</b> member must be set to the total number of bytes allocated for the <b>SYSTEM_MANDATORY_LABEL_ACE</b> structure.


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

Specifies the first <b>DWORD</b> of a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>. The remaining bytes of the <b>SID</b>  are stored in contiguous memory after the <b>SidStart</b> member. The identifier authority of the <b>SID</b> must be <b>SECURITY_MANDATORY_LABEL_AUTHORITY</b>. The <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">RID</a> of the <b>SID</b> specifies the mandatory integrity level of the object associated with the SACL that contains this ACE. The <i>RID</i> must be one of the following values.

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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538866">ACL</a>
 

 


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

# IFaxSecurity::put_InformationType


## -description


The <b>IFaxSecurity::InformationType</b> property represents the security information type.

This property is read/write.


## -parameters


## -remarks



The information type is a bitwise combination that indicates what security information will be retrieved from the server when requesting a security descriptor using the <a href="https://msdn.microsoft.com/a8e4a0c4-324a-4337-a69b-c934bc261b34">IFaxSecurity::Descriptor</a> property or when refreshing the <a href="https://msdn.microsoft.com/e8dabda0-29aa-4ef2-a797-14aae1d8b539">IFaxSecurity</a> object using the <a href="https://msdn.microsoft.com/32e13dff-72a5-4968-9f86-12fff06bd06a">IFaxSecurity::Refresh</a> method. The information type also determines what information is sent to the fax server when you save changes to the <b>IFaxSecurity</b> object using the <a href="https://msdn.microsoft.com/a016aff7-ca25-4724-b13c-92d31da28a38">IFaxSecurity::Save</a> method.

The bits are specified in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff556635">SECURITY_INFORMATION</a> structure, defined in Winnt.h. Each item of security information is designated by a bit flag. The following values specify the bits applicable to the fax service.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>DACL_SECURITY_INFORMATION</td>
<td>Indicates that the discretionary access control list (ACL) of the object is being referenced.</td>
</tr>
<tr>
<td>GROUP_SECURITY_INFORMATION</td>
<td>Indicates that the primary group identifier of the object is being referenced.</td>
</tr>
<tr>
<td>OWNER_SECURITY_INFORMATION</td>
<td>Indicates that the owner identifier of the object is being referenced.</td>
</tr>
<tr>
<td>SACL_SECURITY_INFORMATION</td>
<td>Indicates that the system ACL of the object is being referenced.</td>
</tr>
</table>
 

You should set the <b>IFaxSecurity::InformationType</b> property before you call the <a href="https://msdn.microsoft.com/a8e4a0c4-324a-4337-a69b-c934bc261b34">IFaxSecurity::get_Descriptor</a> method to ensure that you receive the information that you want and to ensure that you request only the information for which you have the appropriate access rights. Also, the <b>IFaxSecurity::InformationType</b> property will affect what information is sent to the fax server when you call the <a href="https://msdn.microsoft.com/a016aff7-ca25-4724-b13c-92d31da28a38">IFaxSecurity::Save</a> method. If you do not set the <b>IFaxSecurity::InformationType</b> property, it defaults to the flags DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, and OWNER_SECURITY_INFORMATION.




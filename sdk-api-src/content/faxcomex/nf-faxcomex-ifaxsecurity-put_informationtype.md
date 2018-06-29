---
UID: NF:faxcomex.IFaxSecurity.put_InformationType
title: IFaxSecurity::put_InformationType
author: windows-sdk-content
description: The InformationType property retrieves the security information type.
old-location: fax\_mfax_faxsecurity_informationtype.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4up1.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxSecurity object [Fax Service],InformationType property, FaxSecurity.InformationType, IFaxSecurity.get_InformationType, IFaxSecurity.put_InformationType, IFaxSecurity::put_InformationType, InformationType property [Fax Service], InformationType property [Fax Service],FaxSecurity object, _mfax_faxsecurity.informationtype, fax._mfax_faxsecurity_informationtype, put_InformationType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
tech.root: 
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - FaxSecurity.InformationType
 - IFaxSecurity.get_InformationType
 - IFaxSecurity.put_InformationType
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxSecurity::put_InformationType


## -description


The <b>InformationType</b> property retrieves the security information type.

This property is read/write.


## -parameters


## -remarks



The information type is a bitwise combination that indicates what security information will be retrieved from the server when requesting a security descriptor using the <a href="https://msdn.microsoft.com/library/Aa358878(v=VS.85).aspx">Descriptor</a> property or when refreshing the <a href="https://msdn.microsoft.com/library/ms689509(v=VS.85).aspx">FaxSecurity</a> object using the <a href="https://msdn.microsoft.com/library/ms690274(v=VS.85).aspx">Refresh</a> method. The information type also determines what information is sent to the fax server when you save changes to the <b>FaxSecurity</b> object using the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a> method.

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
 

You should set the <b>InformationType</b> property before you read the <a href="https://msdn.microsoft.com/library/Aa358878(v=VS.85).aspx">Descriptor</a> property to ensure that you receive the information that you want and to ensure that you request only the information for which you have the appropriate access rights. Also, the <b>InformationType</b> property will affect what information is sent to the fax server when you call the <a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a> method. If you do not set the <b>InformationType</b> property, it defaults to the flags DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, and OWNER_SECURITY_INFORMATION.




---
UID: NF:faxcomex.IFaxSecurity.put_InformationType
title: IFaxSecurity::put_InformationType (faxcomex.h)
description: The IFaxSecurity::InformationType property represents the security information type. (Put)
helpviewer_keywords: ["IFaxSecurity interface [Fax Service]","InformationType property","IFaxSecurity.InformationType","IFaxSecurity.put_InformationType","IFaxSecurity::InformationType","IFaxSecurity::get_InformationType","IFaxSecurity::put_InformationType","InformationType property [Fax Service]","InformationType property [Fax Service]","IFaxSecurity interface","_mfax_faxsecurity.informationtype_cpp","fax._mfax_faxsecurity_informationtype_cpp","faxcomex/IFaxSecurity::InformationType","faxcomex/IFaxSecurity::get_InformationType","faxcomex/IFaxSecurity::put_InformationType","put_InformationType"]
old-location: fax\_mfax_faxsecurity_informationtype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4up1_cpp.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity interface [Fax Service],InformationType property, IFaxSecurity.InformationType, IFaxSecurity.put_InformationType, IFaxSecurity::InformationType, IFaxSecurity::get_InformationType, IFaxSecurity::put_InformationType, InformationType property [Fax Service], InformationType property [Fax Service],IFaxSecurity interface, _mfax_faxsecurity.informationtype_cpp, fax._mfax_faxsecurity_informationtype_cpp, faxcomex/IFaxSecurity::InformationType, faxcomex/IFaxSecurity::get_InformationType, faxcomex/IFaxSecurity::put_InformationType, put_InformationType
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxSecurity::put_InformationType
 - faxcomex/IFaxSecurity::put_InformationType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxSecurity.InformationType
 - IFaxSecurity.get_InformationType
 - IFaxSecurity.put_InformationType
---

# IFaxSecurity::put_InformationType


## -description

The <b>IFaxSecurity::InformationType</b> property represents the security information type.

This property is read/write.

## -parameters

## -remarks

The information type is a bitwise combination that indicates what security information will be retrieved from the server when requesting a security descriptor using the <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxsecurity-get_descriptor">IFaxSecurity::Descriptor</a> property or when refreshing the <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity">IFaxSecurity</a> object using the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity-refresh-vb">IFaxSecurity::Refresh</a> method. The information type also determines what information is sent to the fax server when you save changes to the <b>IFaxSecurity</b> object using the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity-save-vb">IFaxSecurity::Save</a> method.

The bits are specified in the <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure, defined in Winnt.h. Each item of security information is designated by a bit flag. The following values specify the bits applicable to the fax service.

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
 

You should set the <b>IFaxSecurity::InformationType</b> property before you call the <a href="/previous-versions/windows/desktop/api/faxcomex/nf-faxcomex-ifaxsecurity-get_descriptor">IFaxSecurity::get_Descriptor</a> method to ensure that you receive the information that you want and to ensure that you request only the information for which you have the appropriate access rights. Also, the <b>IFaxSecurity::InformationType</b> property will affect what information is sent to the fax server when you call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity-save-vb">IFaxSecurity::Save</a> method. If you do not set the <b>IFaxSecurity::InformationType</b> property, it defaults to the flags DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, and OWNER_SECURITY_INFORMATION.

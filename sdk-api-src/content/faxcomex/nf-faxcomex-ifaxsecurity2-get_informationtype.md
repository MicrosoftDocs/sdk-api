---
UID: NF:faxcomex.IFaxSecurity2.get_InformationType
title: IFaxSecurity2::get_InformationType (faxcomex.h)
description: Retrieves the security information type. (Get)
helpviewer_keywords: ["IFaxSecurity2 interface [Fax Service]","InformationType property","IFaxSecurity2.InformationType","IFaxSecurity2.get_InformationType","IFaxSecurity2.put_InformationType","IFaxSecurity2::InformationType","IFaxSecurity2::get_InformationType","IFaxSecurity2::put_InformationType","InformationType property [Fax Service]","InformationType property [Fax Service]","IFaxSecurity2 interface","_mfax_faxsecurity2.informationtype","fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_informationtype_cpp","fax._mfax_faxsecurity2_informationtype","faxcomex/IFaxSecurity2::InformationType","faxcomex/IFaxSecurity2::get_InformationType","faxcomex/IFaxSecurity2::put_InformationType","get_InformationType"]
old-location: fax\_mfax_faxsecurity2_cpp_mfax_faxsecurity2_informationtype_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\informationtype.htm
ms.date: 12/05/2018
ms.keywords: IFaxSecurity2 interface [Fax Service],InformationType property, IFaxSecurity2.InformationType, IFaxSecurity2.get_InformationType, IFaxSecurity2.put_InformationType, IFaxSecurity2::InformationType, IFaxSecurity2::get_InformationType, IFaxSecurity2::put_InformationType, InformationType property [Fax Service], InformationType property [Fax Service],IFaxSecurity2 interface, _mfax_faxsecurity2.informationtype, fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_informationtype_cpp, fax._mfax_faxsecurity2_informationtype, faxcomex/IFaxSecurity2::InformationType, faxcomex/IFaxSecurity2::get_InformationType, faxcomex/IFaxSecurity2::put_InformationType, get_InformationType
req.header: faxcomex.h
req.include-header: 
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
req.dll: Fxscomex.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxSecurity2::get_InformationType
 - faxcomex/IFaxSecurity2::get_InformationType
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
 - IFaxSecurity2.InformationType
 - IFaxSecurity2.get_InformationType
 - IFaxSecurity2.put_InformationType
 - IFaxSecurity2.get_InformationType
 - IFaxSecurity2.put_InformationType
---

# IFaxSecurity2::get_InformationType


## -description

Retrieves the security information type.

This property is read/write.

## -parameters

## -remarks

The information type is a bitwise combination that indicates what security information will be retrieved from the server when requesting a security descriptor using the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-descriptor">Descriptor</a> property, or when refreshing the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a> object using the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-refresh-vb">IFaxSecurity2::Refresh</a> method. The information type property also determines what information is sent to the fax server when you save changes to the <b>FaxSecurity2</b> object using the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-save-vb">IFaxSecurity2::Save</a> method.

The bits are specified in the <a href="/windows/desktop/SecAuthZ/security-information">SECURITY_INFORMATION</a> structure, defined in Winnt.h. Each item of security information is designated by a bit flag. The following values specify the bits applicable to the fax service:

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
 

Set the <b>IFaxSecurity2::InformationType</b> property before you get the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-descriptor">Descriptor</a> property, to ensure that you receive the desired information, and that you request only the information for which you have the appropriate access rights. Also, the <b>IFaxSecurity2::InformationType</b> property will affect what information is sent to the fax server when you call the <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-save-vb">IFaxSecurity2::Save</a> method. If you do not set the <b>IFaxSecurity2::InformationType</b> property, it defaults to the flags DACL_SECURITY_INFORMATION, GROUP_SECURITY_INFORMATION, and OWNER_SECURITY_INFORMATION.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2">FaxSecurity2</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity2">IFaxSecurity2</a>

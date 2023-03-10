---
UID: NF:faxcomex.IFaxSecurity2.put_Descriptor
title: IFaxSecurity2::put_Descriptor (faxcomex.h)
description: Represents the security descriptor for a IFaxServer2 object. (Put)
helpviewer_keywords: ["Descriptor property [Fax Service]","Descriptor property [Fax Service]","IFaxSecurity2 interface","IFaxSecurity2 interface [Fax Service]","Descriptor property","IFaxSecurity2.Descriptor","IFaxSecurity2.put_Descriptor","IFaxSecurity2::Descriptor","IFaxSecurity2::get_Descriptor","IFaxSecurity2::put_Descriptor","_mfax_faxsecurity2.descriptor_cpp","fax._mfax_faxsecurity2_descriptor_cpp","faxcomex/IFaxSecurity2::Descriptor","faxcomex/IFaxSecurity2::get_Descriptor","faxcomex/IFaxSecurity2::put_Descriptor","put_Descriptor"]
old-location: fax\_mfax_faxsecurity2_descriptor_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\descriptor.htm
ms.date: 12/05/2018
ms.keywords: Descriptor property [Fax Service], Descriptor property [Fax Service],IFaxSecurity2 interface, IFaxSecurity2 interface [Fax Service],Descriptor property, IFaxSecurity2.Descriptor, IFaxSecurity2.put_Descriptor, IFaxSecurity2::Descriptor, IFaxSecurity2::get_Descriptor, IFaxSecurity2::put_Descriptor, _mfax_faxsecurity2.descriptor_cpp, fax._mfax_faxsecurity2_descriptor_cpp, faxcomex/IFaxSecurity2::Descriptor, faxcomex/IFaxSecurity2::get_Descriptor, faxcomex/IFaxSecurity2::put_Descriptor, put_Descriptor
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
 - IFaxSecurity2::put_Descriptor
 - faxcomex/IFaxSecurity2::put_Descriptor
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
 - IFaxSecurity2.Descriptor
 - IFaxSecurity2.get_Descriptor
 - IFaxSecurity2.put_Descriptor
---

# IFaxSecurity2::put_Descriptor


## -description

Represents the security descriptor for a <a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxserver2">IFaxServer2</a> object.

This property is read/write.

## -parameters

## -remarks

The <b>IFaxSecurity2::Descriptor</b> property represents the security descriptor, which contains the rights explicitly granted to a user by the fax administrator. The <a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-grantedrights-vb">IFaxSecurity2::GrantedRights</a> property reflects the user rights that the fax server grants based on the descriptor. Specifically, if a user has the access right <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2SUBMIT_HIGH</a>, the user can send high-priority, normal-priority and low-priority faxes. If a user has the access right <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2SUBMIT_NORMAL</a>, the user can send normal-priority and low-priority faxes.

To read and write this property, the user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2MANAGE_CONFIG</a> access right. Users with the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum_2">far2QUERY_CONFIG</a> access right can read this property.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxsecurity2-descriptor">FaxSecurity2.Descriptor</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxsecurity2">IFaxSecurity2</a>

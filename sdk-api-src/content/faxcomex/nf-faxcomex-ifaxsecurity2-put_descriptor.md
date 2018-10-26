---
UID: NF:faxcomex.IFaxSecurity2.put_Descriptor
title: IFaxSecurity2::put_Descriptor
author: windows-sdk-content
description: Represents the security descriptor for a IFaxServer2 object.
old-location: fax\_mfax_faxsecurity2_descriptor_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\descriptor.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: Descriptor property [Fax Service], Descriptor property [Fax Service],IFaxSecurity2 interface, IFaxSecurity2 interface [Fax Service],Descriptor property, IFaxSecurity2.Descriptor, IFaxSecurity2.put_Descriptor, IFaxSecurity2::Descriptor, IFaxSecurity2::get_Descriptor, IFaxSecurity2::put_Descriptor, _mfax_faxsecurity2.descriptor_cpp, fax._mfax_faxsecurity2_descriptor_cpp, faxcomex/IFaxSecurity2::Descriptor, faxcomex/IFaxSecurity2::get_Descriptor, faxcomex/IFaxSecurity2::put_Descriptor, put_Descriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSecurity2::put_Descriptor


## -description


Represents the security descriptor for a <a href="https://msdn.microsoft.com/1b049d0c-f7dc-4563-8002-4f711f584577">IFaxServer2</a> object.

This property is read/write.


## -parameters


## -remarks



The <b>IFaxSecurity2::Descriptor</b> property represents the security descriptor, which contains the rights explicitly granted to a user by the fax administrator. The <a href="https://msdn.microsoft.com/c7a839d9-d7d5-4942-8886-b1ca494c5842">IFaxSecurity2::GrantedRights</a> property reflects the user rights that the fax server grants based on the descriptor. Specifically, if a user has the access right <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2SUBMIT_HIGH</a>, the user can send high-priority, normal-priority and low-priority faxes. If a user has the access right <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2SUBMIT_NORMAL</a>, the user can send normal-priority and low-priority faxes.

To read and write this property, the user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_CONFIG</a> access right. Users with the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_CONFIG</a> access right can read this property.  




## -see-also




<a href="https://msdn.microsoft.com/9fda9779-6688-431c-8f06-8420d0263e0d">FaxSecurity2.Descriptor</a>



<a href="https://msdn.microsoft.com/a6238a8f-3e19-4dd8-b602-525774d671df">IFaxSecurity2</a>
 

 


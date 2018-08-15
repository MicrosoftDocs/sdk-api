---
UID: NF:faxcomex.IFaxSecurity2.get_Descriptor
title: IFaxSecurity2::get_Descriptor
author: windows-sdk-content
description: Represents the security descriptor for a IFaxServer2 interface.
old-location: fax\_mfax_faxsecurity2_descriptor.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\o\faxsecurity2\faxinto_z_descriptor.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Descriptor property [Fax Service], Descriptor property [Fax Service],FaxSecurity2 object, FaxSecurity2 object [Fax Service],Descriptor property, FaxSecurity2.Descriptor, IFaxSecurity2.get_Descriptor, IFaxSecurity2.put_Descriptor, IFaxSecurity2::get_Descriptor, _mfax_faxsecurity2.descriptor, fax._mfax_faxsecurity2_descriptor, get_Descriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.redist: 
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
 - FaxSecurity2.Descriptor
 - IFaxSecurity2.get_Descriptor
 - IFaxSecurity2.put_Descriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxSecurity2::get_Descriptor


## -description


Represents the security descriptor for a <a href="https://msdn.microsoft.com/en-us/library/Aa358976(v=VS.85).aspx">IFaxServer2</a> interface.

This property is read/write.


## -parameters


## -remarks



The <b>Descriptor</b> property represents the security descriptor, which contains the rights explicitly granted to a user by the fax administrator. The <a href="https://msdn.microsoft.com/en-us/library/Aa358980(v=VS.85).aspx">GrantedRights</a> property reflects the user rights that the fax server grants based on the descriptor. Specifically, if a user has the access right <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2SUBMIT_HIGH</a>, the user can send high-priority, normal-priority and low-priority faxes. If a user has the access right <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2SUBMIT_NORMAL</a>, the user can send normal-priority and low-priority faxes.

To read and write this property, the user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2MANAGE_CONFIG</a> access right. Users with the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2QUERY_CONFIG</a> access right can read this property.  




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa358873(v=VS.85).aspx">FaxSecurity2</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358978(v=VS.85).aspx">IFaxSecurity2::Descriptor</a>
 

 


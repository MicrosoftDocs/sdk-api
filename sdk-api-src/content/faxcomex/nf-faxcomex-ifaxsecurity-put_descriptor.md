---
UID: NF:faxcomex.IFaxSecurity.put_Descriptor
title: IFaxSecurity::put_Descriptor
author: windows-sdk-content
description: The Descriptor property represents the security descriptor for a FaxServer object.
old-location: fax\_mfax_faxsecurity_descriptor.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\o\faxsecurity\faxinto_z_6ab6.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: Descriptor property [Fax Service], Descriptor property [Fax Service],FaxSecurity object, FaxSecurity object [Fax Service],Descriptor property, FaxSecurity.Descriptor, IFaxSecurity.get_Descriptor, IFaxSecurity.put_Descriptor, IFaxSecurity::put_Descriptor, _mfax_faxsecurity.descriptor, fax._mfax_faxsecurity_descriptor, put_Descriptor
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
 - FaxSecurity.Descriptor
 - IFaxSecurity.get_Descriptor
 - IFaxSecurity.put_Descriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxSecurity::put_Descriptor


## -description


The <b>Descriptor</b> property represents the security descriptor for a <a href="https://msdn.microsoft.com/df3aa427-9d29-4024-a6d5-ed5fd8dba36c">FaxServer</a> object.

This property is read/write.


## -parameters


## -remarks



The <b>Descriptor</b> property represents the security descriptor, which contains the rights explicitly granted to a user by the fax administrator. The <a href="https://msdn.microsoft.com/7fd4d1c0-3980-410a-8150-34461cbff59c">GrantedRights</a> property reflects the user rights that the fax server grants based on the descriptor. Specifically, if a user has the access right <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_HIGH</a>, the user can send high-priority, normal-priority and low-priority faxes. If a user has the access right <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_NORMAL</a>, the user can send normal-priority and low-priority faxes.

To read this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/0c1fe69c-f10b-4c7d-abe5-1a3e93d56c04">FaxSecurity</a>



<a href="https://msdn.microsoft.com/a8e4a0c4-324a-4337-a69b-c934bc261b34">IFaxSecurity::Descriptor</a>
 

 


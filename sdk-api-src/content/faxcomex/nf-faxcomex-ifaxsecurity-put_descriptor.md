---
UID: NF:faxcomex.IFaxSecurity.put_Descriptor
title: IFaxSecurity::put_Descriptor
author: windows-driver-content
description: The Descriptor property represents the security descriptor for a IFaxServer object.
old-location: fax\_mfax_faxsecurity_descriptor_cpp.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\descriptor.htm
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: Descriptor property [Fax Service], Descriptor property [Fax Service],IFaxSecurity interface, IFaxSecurity interface [Fax Service],Descriptor property, IFaxSecurity.Descriptor, IFaxSecurity.put_Descriptor, IFaxSecurity::Descriptor, IFaxSecurity::get_Descriptor, IFaxSecurity::put_Descriptor, _mfax_faxsecurity.descriptor_cpp, fax._mfax_faxsecurity_descriptor_cpp, faxcomex/IFaxSecurity::Descriptor, faxcomex/IFaxSecurity::get_Descriptor, faxcomex/IFaxSecurity::put_Descriptor, put_Descriptor
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FAX_SMTP_AUTHENTICATION_TYPE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fxscomex.dll
api_name:
-	IFaxSecurity.Descriptor
-	IFaxSecurity.get_Descriptor
-	IFaxSecurity.put_Descriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxSecurity::put_Descriptor


## -description


The <b>Descriptor</b> property  represents the security descriptor for a <a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a> object.

This property is read/write.


## -parameters


## -remarks



The <b>IFaxSecurity::Descriptor</b> property represents the security descriptor, which contains the rights explicitly granted to a user by the fax administrator. The <a href="https://msdn.microsoft.com/329c4bd1-6b92-4dbf-aaf9-2e8c89192fd6">IFaxSecurity::get_GrantedRights</a> property reflects the user rights that the fax server grants based on the descriptor. Specifically, if a user has the access right <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_HIGH</a>, the user can send high-priority, normal-priority and low-priority faxes. If a user has the access right <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_NORMAL</a>, the user can send normal-priority and low-priority faxes.

To read this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/66911dcd-2c46-4ef3-ae77-cb94249e92e3">FaxSecurity.Descriptor</a>



<a href="https://msdn.microsoft.com/e8dabda0-29aa-4ef2-a797-14aae1d8b539">IFaxSecurity</a>
 

 


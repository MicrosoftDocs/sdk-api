---
UID: NF:faxcomex.IFaxSecurity.get_GrantedRights
title: IFaxSecurity::get_GrantedRights
author: windows-sdk-content
description: The IFaxSecurity::get_GrantedRights property is a combination of the fax server access rights granted to the user referencing this property.
old-location: fax\_mfax_faxsecurity_cpp_mfax_faxsecurity_grantedrights_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_4wab.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GrantedRights property [Fax Service], GrantedRights property [Fax Service],IFaxSecurity interface, IFaxSecurity interface [Fax Service],GrantedRights property, IFaxSecurity.GrantedRights, IFaxSecurity.get_GrantedRights, IFaxSecurity::GrantedRights, IFaxSecurity::get_GrantedRights, _mfax_faxsecurity.grantedrights, fax._mfax_faxsecurity_cpp_mfax_faxsecurity_grantedrights_cpp, fax._mfax_faxsecurity_grantedrights, faxcomex/IFaxSecurity::GrantedRights, faxcomex/IFaxSecurity::get_GrantedRights, get_GrantedRights
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
 - IFaxSecurity.GrantedRights
 - IFaxSecurity.get_GrantedRights
 - IFaxSecurity.get_GrantedRights
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSecurity::get_GrantedRights


## -description


The <b>IFaxSecurity::get_GrantedRights</b> property is a combination of the fax server access rights granted to the user referencing this property. For example, some users have permission to submit fax jobs with high priority while others have permission to submit jobs with normal or low priority only.

This property is read-only.


## -parameters


## -remarks



The <b>IFaxSecurity::get_GrantedRights</b> property reflects rights granted by the fax server, while the <a href="https://msdn.microsoft.com/a8e4a0c4-324a-4337-a69b-c934bc261b34">IFaxSecurity::Descriptor</a> property represents the security descriptor, which contains the rights explicitly granted to a user by the fax administrator.

To read this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/0c1fe69c-f10b-4c7d-abe5-1a3e93d56c04">FaxSecurity</a>



<a href="https://msdn.microsoft.com/e8dabda0-29aa-4ef2-a797-14aae1d8b539">IFaxSecurity</a>
 

 


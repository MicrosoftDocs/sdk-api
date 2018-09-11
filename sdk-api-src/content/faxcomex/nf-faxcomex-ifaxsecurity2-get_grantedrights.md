---
UID: NF:faxcomex.IFaxSecurity2.get_GrantedRights
title: IFaxSecurity2::get_GrantedRights
author: windows-sdk-content
description: Retrieves a combination of the fax server access rights granted to the user referencing this property.
old-location: fax\_mfax_faxsecurity2_cpp_mfax_faxsecurity2_grantedrights_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxsecurity2\grantedrights.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: GrantedRights property [Fax Service], GrantedRights property [Fax Service],IFaxSecurity2 interface, IFaxSecurity2 interface [Fax Service],GrantedRights property, IFaxSecurity2.GrantedRights, IFaxSecurity2.get_GrantedRights, IFaxSecurity2::GrantedRights, IFaxSecurity2::get_GrantedRights, _mfax_faxsecurity2.grantedrights, fax._mfax_faxsecurity2_cpp_mfax_faxsecurity2_grantedrights_cpp, fax._mfax_faxsecurity2_grantedrights, faxcomex/IFaxSecurity2::GrantedRights, faxcomex/IFaxSecurity2::get_GrantedRights, get_GrantedRights
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
 - IFaxSecurity2.GrantedRights
 - IFaxSecurity2.get_GrantedRights
 - IFaxSecurity2.get_GrantedRights
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSecurity2::get_GrantedRights


## -description


Retrieves a combination of the fax server access rights granted to the user referencing this property. For example, some users have permission to submit fax jobs with high priority while others have permission to submit jobs with normal or low priority only.

This property is read-only.


## -parameters


## -remarks



The <b>IFaxSecurity2::GrantedRights</b> property reflects rights granted by the fax server, while the <a href="https://msdn.microsoft.com/9fda9779-6688-431c-8f06-8420d0263e0d">Descriptor</a> property represents the security descriptor, which contains the rights explicitly granted to a user by the fax administrator.

To read this property, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/213e555a-1509-4081-a21b-f33fc4653f32">FaxSecurity2</a>



<a href="https://msdn.microsoft.com/a6238a8f-3e19-4dd8-b602-525774d671df">IFaxSecurity2</a>
 

 


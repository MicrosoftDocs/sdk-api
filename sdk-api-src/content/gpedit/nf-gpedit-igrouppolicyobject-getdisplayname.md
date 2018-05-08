---
UID: NF:gpedit.IGroupPolicyObject.GetDisplayName
title: IGroupPolicyObject::GetDisplayName
author: windows-driver-content
description: The GetDisplayName method retrieves the display name for the GPO.
old-location: policy\igrouppolicyobject_getdisplayname.htm
old-project: Policy
ms.assetid: a16592c3-8fa1-4859-b379-ef31999a3fdd
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: GetDisplayName, GetDisplayName method [Group Policy], GetDisplayName method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetDisplayName method, IGroupPolicyObject.GetDisplayName, IGroupPolicyObject::GetDisplayName, _win32_igrouppolicyobject_getdisplayname, gpedit/IGroupPolicyObject::GetDisplayName, policy.igrouppolicyobject_getdisplayname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IGroupPolicyObject.GetDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::GetDisplayName


## -description


The
    <b>GetDisplayName</b> method retrieves the display name for the GPO.


## -parameters




### -param pszName [out]

Pointer to a buffer that receives the display name.


### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To set the display name for a GPO, you can call the 
<a href="https://msdn.microsoft.com/979e8399-83e1-421e-8f32-813464ac97aa">SetDisplayName</a> method. Call 
<a href="https://msdn.microsoft.com/1374c01c-aba3-48f5-8a42-7139873d8f7c">GetName</a> to retrieve the unique name for a GPO, which is a GUID for an Active Directory object.




## -see-also




<a href="https://msdn.microsoft.com/1374c01c-aba3-48f5-8a42-7139873d8f7c">GetName</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>



<a href="https://msdn.microsoft.com/979e8399-83e1-421e-8f32-813464ac97aa">SetDisplayName</a>
 

 


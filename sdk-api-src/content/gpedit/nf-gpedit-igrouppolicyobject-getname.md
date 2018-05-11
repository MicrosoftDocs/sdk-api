---
UID: NF:gpedit.IGroupPolicyObject.GetName
title: IGroupPolicyObject::GetName
author: windows-driver-content
description: The GetName method retrieves the unique GPO name.
old-location: policy\igrouppolicyobject_getname.htm
old-project: Policy
ms.assetid: 1374c01c-aba3-48f5-8a42-7139873d8f7c
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetName, GetName method [Group Policy], GetName method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetName method, IGroupPolicyObject.GetName, IGroupPolicyObject::GetName, _win32_igrouppolicyobject_getname, gpedit/IGroupPolicyObject::GetName, policy.igrouppolicyobject_getname
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
-	IGroupPolicyObject.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::GetName


## -description


The
    <b>GetName</b> method retrieves the unique GPO name.

For Active Directory policy objects, the method returns a GUID. For a local GPO, the method returns the string "Local". For remote objects, 
<b>GetName</b> returns the computer name.


## -parameters




### -param pszName [out]

Pointer to a buffer that receives the GPO name.


### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To retrieve the display name for a GPO, you can call the 
<a href="https://msdn.microsoft.com/a16592c3-8fa1-4859-b379-ef31999a3fdd">GetDisplayName</a> method.




## -see-also




<a href="https://msdn.microsoft.com/a16592c3-8fa1-4859-b379-ef31999a3fdd">GetDisplayName</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 


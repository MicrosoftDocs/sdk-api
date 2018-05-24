---
UID: NF:gpedit.IGroupPolicyObject.Delete
title: IGroupPolicyObject::Delete
author: windows-driver-content
description: The Delete method deletes the GPO.
old-location: policy\igrouppolicyobject_delete.htm
old-project: Policy
ms.assetid: 34afb04e-47f9-4d7c-9fa6-9d76188d7e05
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: Delete, Delete method [Group Policy], Delete method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],Delete method, IGroupPolicyObject.Delete, IGroupPolicyObject::Delete, _win32_igrouppolicyobject_delete, gpedit/IGroupPolicyObject::Delete, policy.igrouppolicyobject_delete
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
-	IGroupPolicyObject.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::Delete


## -description


The
    <b>Delete</b> method deletes the GPO.


## -parameters






## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



After calling this method, you cannot call other methods of the 
<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a> interface because all data has been deleted for the GPO.

<div class="alert"><b>Note</b>  A policy refresh will not automatically be triggered when the local Group Policy object is deleted using the <b>Delete</b> method.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn926944">Save</a>
 

 


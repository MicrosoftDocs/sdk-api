---
UID: NF:gpedit.IGroupPolicyObject.SetDisplayName
title: IGroupPolicyObject::SetDisplayName
author: windows-sdk-content
description: The SetDisplayName method sets the display name for the GPO.
old-location: policy\igrouppolicyobject_setdisplayname.htm
old-project: Policy
ms.assetid: 979e8399-83e1-421e-8f32-813464ac97aa
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IGroupPolicyObject interface [Group Policy],SetDisplayName method, IGroupPolicyObject.SetDisplayName, IGroupPolicyObject::SetDisplayName, SetDisplayName, SetDisplayName method [Group Policy], SetDisplayName method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_setdisplayname, gpedit/IGroupPolicyObject::SetDisplayName, policy.igrouppolicyobject_setdisplayname
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.SetDisplayName
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::SetDisplayName


## -description


The
    <b>SetDisplayName</b> method sets the display name for the GPO.


## -parameters




### -param pszName [in]

Specifies the new display name.


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
 

 


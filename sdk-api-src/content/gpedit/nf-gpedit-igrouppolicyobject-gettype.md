---
UID: NF:gpedit.IGroupPolicyObject.GetType
title: IGroupPolicyObject::GetType
author: windows-sdk-content
description: The GetType method retrieves type information for the GPO being edited.
old-location: policy\igrouppolicyobject_gettype.htm
tech.root: Policy
ms.assetid: e64314aa-340f-496c-aa6b-4744573565f6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GPOTypeDS, GPOTypeLocal, GPOTypeRemote, GetType, GetType method [Group Policy], GetType method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetType method, IGroupPolicyObject.GetType, IGroupPolicyObject::GetType, _win32_igrouppolicyobject_gettype, gpedit/IGroupPolicyObject::GetType, policy.igrouppolicyobject_gettype
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
req.lib: 
req.dll: Gpedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.GetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGroupPolicyObject::GetType


## -description


The
    <b>GetType</b> method retrieves type information for the GPO being edited.


## -parameters




### -param gpoType [out]

Receives the GPO type. The system sets this parameter to one of the following values.



#### GPOTypeDS

Active Directory



#### GPOTypeLocal

Local



#### GPOTypeRemote

Remote


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 


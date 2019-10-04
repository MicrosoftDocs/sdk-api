---
UID: NF:gpedit.IGroupPolicyObject.GetType
title: IGroupPolicyObject::GetType (gpedit.h)
author: windows-sdk-content
description: The GetType method retrieves type information for the GPO being edited.
old-location: policy\igrouppolicyobject_gettype.htm
tech.root: Policy
ms.assetid: e64314aa-340f-496c-aa6b-4744573565f6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPOTypeDS, GPOTypeLocal, GPOTypeRemote, GetType, GetType method [Group Policy], GetType method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetType method, IGroupPolicyObject.GetType, IGroupPolicyObject::GetType, _win32_igrouppolicyobject_gettype, gpedit/IGroupPolicyObject::GetType, policy.igrouppolicyobject_gettype
ms.topic: method
f1_keywords: 
 - "gpedit/IGroupPolicyObject.GetType"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>
 

 


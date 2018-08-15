---
UID: NF:gpedit.IGroupPolicyObject.GetMachineName
title: IGroupPolicyObject::GetMachineName
author: windows-sdk-content
description: The GetMachineName method retrieves the computer name of the remote GPO. This is the name specified by the OpenRemoteMachineGPO method.
old-location: policy\igrouppolicyobject_getmachinename.htm
old-project: Policy
ms.assetid: 6ac20718-45d4-4a45-a95e-d159e4d6dacc
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetMachineName, GetMachineName method [Group Policy], GetMachineName method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetMachineName method, IGroupPolicyObject.GetMachineName, IGroupPolicyObject::GetMachineName, _win32_igrouppolicyobject_getmachinename, gpedit/IGroupPolicyObject::GetMachineName, policy.igrouppolicyobject_getmachinename
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
 - IGroupPolicyObject.GetMachineName
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject::GetMachineName


## -description


The
    <b>GetMachineName</b> method retrieves the computer name of the remote GPO. This is the name specified by the 
<a href="https://msdn.microsoft.com/ac124b48-7eb6-473b-a96b-de9b1a903f28">OpenRemoteMachineGPO</a> method.


## -parameters




### -param pszName [out]

Pointer to a buffer that receives the computer name.


### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>



<a href="https://msdn.microsoft.com/ac124b48-7eb6-473b-a96b-de9b1a903f28">OpenRemoteMachineGPO</a>
 

 


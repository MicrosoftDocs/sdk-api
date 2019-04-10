---
UID: NF:userenv.RsopResetPolicySettingStatus
title: RsopResetPolicySettingStatus function (userenv.h)
author: windows-sdk-content
description: The RSoPResetPolicySettingStatus function unlinks the RSOP_PolicySettingStatus instance from its RSOP_PolicySetting instance.
old-location: policy\rsopresetpolicysettingstatus.htm
tech.root: Policy
ms.assetid: fd849efe-1ee7-4034-aea2-1a2bdb5e46bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RSoPResetPolicySettingStatus, RSoPResetPolicySettingStatus function [Group Policy], RsopResetPolicySettingStatus, _win32_rsopresetpolicysettingstatus, policy.rsopresetpolicysettingstatus, userenv/RSoPResetPolicySettingStatus
ms.topic: function
req.header: userenv.h
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
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - RSoPResetPolicySettingStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RsopResetPolicySettingStatus function


## -description


The 
    <b>RSoPResetPolicySettingStatus</b> function unlinks the 
<a href="https://msdn.microsoft.com/b3dfd62a-c461-4f9b-95cb-3ef944c51024">RSOP_PolicySettingStatus</a> instance from its 
<a href="https://msdn.microsoft.com/131b0f68-5c39-402b-a8e2-c111e852f1cb">RSOP_PolicySetting</a> instance. The function deletes the instances of 
<b>RSOP_PolicySettingStatus</b> and 
<a href="https://msdn.microsoft.com/359e7212-a5ba-42eb-b704-8c838cdce24b">RSOP_PolicySettingLink</a>. Optionally, you can also specify that the function delete the instance of 
<b>RSOP_PolicySetting</b>.


## -parameters




### -param dwFlags [in]

This parameter is currently unused.


### -param pServices [in]

Specifies a WMI services pointer to the RSoP namespace to which the policy data is to be written. This parameter is required.


### -param pSettingInstance [in]

Pointer to an instance of 
<a href="https://msdn.microsoft.com/131b0f68-5c39-402b-a8e2-c111e852f1cb">RSOP_PolicySetting</a> containing the policy setting. This parameter is required and can also point to the instance's children.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To link (associate) the 
<a href="https://msdn.microsoft.com/b3dfd62a-c461-4f9b-95cb-3ef944c51024">RSOP_PolicySettingStatus</a> instance to its 
<a href="https://msdn.microsoft.com/131b0f68-5c39-402b-a8e2-c111e852f1cb">RSOP_PolicySetting</a> instance, you can call the 
<a href="https://msdn.microsoft.com/7ea2f217-4dd2-4c0f-af1b-d4bcb8707519">RSoPSetPolicySettingStatus</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/7ea2f217-4dd2-4c0f-af1b-d4bcb8707519">RSoPSetPolicySettingStatus</a>
 

 


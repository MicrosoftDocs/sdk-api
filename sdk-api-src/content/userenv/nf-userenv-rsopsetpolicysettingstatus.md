---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RsopSetPolicySettingStatus function


## -description


The 
    <b>RSoPSetPolicySettingStatus</b> function creates an instance of 
<a href="https://msdn.microsoft.com/b3dfd62a-c461-4f9b-95cb-3ef944c51024">RSOP_PolicySettingStatus</a> and an instance of 
<a href="https://msdn.microsoft.com/359e7212-a5ba-42eb-b704-8c838cdce24b">RSOP_PolicySettingLink</a>. The function links (associates) 
<b>RSOP_PolicySettingStatus</b> to its 
<a href="https://msdn.microsoft.com/131b0f68-5c39-402b-a8e2-c111e852f1cb">RSOP_PolicySetting</a> instance.


## -parameters




### -param dwFlags [in]

This parameter is currently unused.


### -param pServices [in]

Specifies a WMI services pointer to the RSoP namespace to which the policy data is to be written. This parameter is required.


### -param pSettingInstance [in]

Pointer to an instance of 
<a href="https://msdn.microsoft.com/131b0f68-5c39-402b-a8e2-c111e852f1cb">RSOP_PolicySetting</a> containing the policy setting. This parameter is required and can point to the instance's children.


### -param nInfo [in]

Specifies the number of elements in the <i>pStatus</i> array.


### -param pStatus [in]

Pointer to an array of 
<a href="https://msdn.microsoft.com/f86dbd35-9180-43f1-ad66-7dba31e1fc89">POLICYSETTINGSTATUSINFO</a> structures.


## -returns



If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To unlink an 
<a href="https://msdn.microsoft.com/b3dfd62a-c461-4f9b-95cb-3ef944c51024">RSOP_PolicySettingStatus</a> instance from its 
<a href="https://msdn.microsoft.com/131b0f68-5c39-402b-a8e2-c111e852f1cb">RSOP_PolicySetting</a> instance, you can call the 
<a href="https://msdn.microsoft.com/fd849efe-1ee7-4034-aea2-1a2bdb5e46bc">RSoPResetPolicySettingStatus</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7c45666e-d7c7-4989-ad19-b1b230757a88">Group Policy
    Functions</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a>



<a href="https://msdn.microsoft.com/fd849efe-1ee7-4034-aea2-1a2bdb5e46bc">RSoPResetPolicySettingStatus</a>
 

 


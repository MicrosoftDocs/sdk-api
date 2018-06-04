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

# IFhConfigMgr::GetLocalPolicy


## -description


Retrieves the numeric parameter for a local policy for the File History feature.


## -parameters




### -param LocalPolicyType [in]

Specifies the local policy.


### -param PolicyValue [out]

Receives the value of the numeric parameter for the specified local policy.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



Each local policy contains a numeric parameter that specifies how or when the File History feature backs up files and folders. See the <a href="https://msdn.microsoft.com/59C54A67-91A3-495F-95F2-50EB373D442C">FH_LOCAL_POLICY_TYPE</a> enumeration for more information about the local policies that can be specified.

To set the numeric parameter value for a local policy, use the <a href="https://msdn.microsoft.com/A1106349-6B14-4A44-B845-7853FA1919D6">IFhConfigMgr::SetLocalPolicy</a> method.




## -see-also




<a href="https://msdn.microsoft.com/59C54A67-91A3-495F-95F2-50EB373D442C">FH_LOCAL_POLICY_TYPE</a>



<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/A1106349-6B14-4A44-B845-7853FA1919D6">IFhConfigMgr::SetLocalPolicy</a>
 

 


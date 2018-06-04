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

# CoAllowUnmarshalerCLSID function


## -description


Adds an unmarshaler CLSID to the allowed list for the calling process only.


## -parameters




### -param clsid [in]

The CLSID of the unmarshaler to be added to the per-process allowed list.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Don't call the <b>CoAllowUnmarshalerCLSID</b> function until after <a href="https://msdn.microsoft.com/e0933741-6b75-4ce1-aa63-6240e4a7130f">CoInitializeSecurity</a> has been called in the current process.

The <b>CoAllowUnmarshalerCLSID</b> function provides more granular control over unmarshaling policy than is provided by the policy options. If the process applies any unmarshaling policy, the effect of the <b>CoAllowUnmarshalerCLSID</b> function is to make the policy comparatively weaker. For this reason, only call <b>CoAllowUnmarshalerCLSID</b> when the security impact is well understood. Usually, this is used to facilitate applying a stronger unmarshaling policy option for the broad attack surface reduction this provides, when a specific unmarshaler CLSID not allowed by that option is needed due to other constraints.

For example, it's appropriate to call the <b>CoAllowUnmarshalerCLSID</b> function when an unmarshaler is known or believed to have a vulnerability but is required by an app. Also, it's appropriate to call <b>CoAllowUnmarshalerCLSID</b> if the unmarshaler is used in multiple processes, but only as part of an uncommon feature. Don't use the <b>CoAllowUnmarshalerCLSID</b> function as a replacement for hardening the unmarshaler. 




## -see-also




<a href="https://msdn.microsoft.com/7F557290-7162-4B32-880B-9A445A083F91">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a>



<a href="https://msdn.microsoft.com/7C4A3982-3623-4F1F-929C-6D0503700450">IMarshalingStream</a>
 

 


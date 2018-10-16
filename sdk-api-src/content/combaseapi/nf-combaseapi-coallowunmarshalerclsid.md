---
UID: NF:combaseapi.CoAllowUnmarshalerCLSID
title: CoAllowUnmarshalerCLSID function
author: windows-sdk-content
description: Adds an unmarshaler CLSID to the allowed list for the calling process only.
old-location: com\coallowunmarshalerclsid.htm
tech.root: com
ms.assetid: 4655C6B6-02CE-42B2-A157-0C0325D1BE52
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: CoAllowUnmarshalerCLSID, CoAllowUnmarshalerCLSID function [COM], com.coallowunmarshalerclsid, combaseapi/CoAllowUnmarshalerCLSID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: combaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
api_name:
 - CoAllowUnmarshalerCLSID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 


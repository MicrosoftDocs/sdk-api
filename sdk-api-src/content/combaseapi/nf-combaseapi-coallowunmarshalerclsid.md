---
UID: NF:combaseapi.CoAllowUnmarshalerCLSID
title: CoAllowUnmarshalerCLSID function (combaseapi.h)
description: Adds an unmarshaler CLSID to the allowed list for the calling process only.
helpviewer_keywords: ["CoAllowUnmarshalerCLSID","CoAllowUnmarshalerCLSID function [COM]","com.coallowunmarshalerclsid","combaseapi/CoAllowUnmarshalerCLSID"]
old-location: com\coallowunmarshalerclsid.htm
tech.root: com
ms.assetid: 4655C6B6-02CE-42B2-A157-0C0325D1BE52
ms.date: 12/05/2018
ms.keywords: CoAllowUnmarshalerCLSID, CoAllowUnmarshalerCLSID function [COM], com.coallowunmarshalerclsid, combaseapi/CoAllowUnmarshalerCLSID
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoAllowUnmarshalerCLSID
 - combaseapi/CoAllowUnmarshalerCLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
api_name:
 - CoAllowUnmarshalerCLSID
---

# CoAllowUnmarshalerCLSID function


## -description

Adds an unmarshaler CLSID to the allowed list for the calling process only.

## -parameters

### -param clsid [in]

The CLSID of the unmarshaler to be added to the per-process allowed list.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Don't call the <b>CoAllowUnmarshalerCLSID</b> function until after <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity">CoInitializeSecurity</a> has been called in the current process.

The <b>CoAllowUnmarshalerCLSID</b> function provides more granular control over unmarshaling policy than is provided by the policy options. If the process applies any unmarshaling policy, the effect of the <b>CoAllowUnmarshalerCLSID</b> function is to make the policy comparatively weaker. For this reason, only call <b>CoAllowUnmarshalerCLSID</b> when the security impact is well understood. Usually, this is used to facilitate applying a stronger unmarshaling policy option for the broad attack surface reduction this provides, when a specific unmarshaler CLSID not allowed by that option is needed due to other constraints.

For example, it's appropriate to call the <b>CoAllowUnmarshalerCLSID</b> function when an unmarshaler is known or believed to have a vulnerability but is required by an app. Also, it's appropriate to call <b>CoAllowUnmarshalerCLSID</b> if the unmarshaler is used in multiple processes, but only as part of an uncommon feature. Don't use the <b>CoAllowUnmarshalerCLSID</b> function as a replacement for hardening the unmarshaler.

## -see-also

<a href="/windows/win32/api/objidl/ne-objidl-globalopt_unmarshaling_policy_values">GLOBALOPT_UNMARSHALING_POLICY_VALUES</a>



<a href="/windows/desktop/api/objidl/nn-objidl-imarshalingstream">IMarshalingStream</a>
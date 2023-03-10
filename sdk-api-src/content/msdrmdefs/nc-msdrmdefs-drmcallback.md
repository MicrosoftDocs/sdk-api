---
UID: NC:msdrmdefs.DRMCALLBACK
title: DRMCALLBACK (msdrmdefs.h)
description: Some of the functions included in the AD RMS SDK provide status information and licenses to your application by using a callback function that you must implement. The callback syntax is shown below.
helpviewer_keywords: ["DRM callback","DRMCallback","DRMCallback callback function [Active Directory Rights Management Services SDK 1.0]","msdrmdefs/DRMCallback","rm.callback_prototype"]
old-location: rm\callback_prototype.htm
tech.root: rm
ms.assetid: 41c200df-afbc-43a5-8046-d131fec3261a
ms.date: 12/05/2018
ms.keywords: DRM callback, DRMCallback, DRMCallback callback function [Active Directory Rights Management Services SDK 1.0], msdrmdefs/DRMCallback, rm.callback_prototype
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMCALLBACK
 - msdrmdefs/DRMCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Msdrmdefs.h
api_name:
 - DRMCallback
---

# DRMCALLBACK callback function


## -description

>[!Note]
>The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, which leverages functionality exposed by the client in Msipc.dll.

Some of the functions included in the AD RMS SDK provide status information and licenses to your application by using a callback function that you must implement. The callback syntax is shown below.

## -parameters

### -param unnamedParam1

Specifies the action being performed. This can be one of the <a href="/windows/desktop/api/msdrmdefs/ne-msdrmdefs-drm_status_msg">DRM_STATUS_MSG</a> enumeration values.

### -param unnamedParam2

The status of the current action.

### -param 

An application-defined value, such as a pointer to a callback function or a pointer to an event handle.


#### - pvParam

This parameter depends on the action being processed. For more information, see the specific message value in the <a href="/windows/desktop/api/msdrmdefs/ne-msdrmdefs-drm_status_msg">DRM_STATUS_MSG</a> enumeration.

## -returns

 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

The following asynchronous AD RMS functions use a callback function:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetsignedissuancelicense">DRMGetSignedIssuanceLicense</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquireadvisories">DRMAcquireAdvisories</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmacquirelicense">DRMAcquireLicense</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a>
</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/creating-a-callback-function">Creating a Callback Function</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/end-user-license-callback-example">End-User License Callback Example</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/issuance-license-callback-example">Issuance License Callback Example</a>

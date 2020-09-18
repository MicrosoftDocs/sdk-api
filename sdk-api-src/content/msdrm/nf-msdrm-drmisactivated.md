---
UID: NF:msdrm.DRMIsActivated
title: DRMIsActivated function (msdrm.h)
description: Indicates whether the current user or machine is activated.
helpviewer_keywords: ["DRMIsActivated","DRMIsActivated function [Active Directory Rights Management Services SDK 1.0]","DRM_ACTIVATE_GROUPIDENTITY","DRM_ACTIVATE_MACHINE","msdrm/DRMIsActivated","rm.drmisactivated"]
old-location: rm\drmisactivated.htm
tech.root: rm
ms.assetid: f6c7bc7f-e9e8-4fc4-b30f-31bc0f5f46aa
ms.date: 12/05/2018
ms.keywords: DRMIsActivated, DRMIsActivated function [Active Directory Rights Management Services SDK 1.0], DRM_ACTIVATE_GROUPIDENTITY, DRM_ACTIVATE_MACHINE, msdrm/DRMIsActivated, rm.drmisactivated
req.header: msdrm.h
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
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMIsActivated
 - msdrm/DRMIsActivated
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMIsActivated
---

# DRMIsActivated function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMIsActivated</b> function indicates whether the current user or machine is activated.

## -parameters

### -param hClient [in]

A handle to a client session created by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a> function.

### -param uFlags [in]

A value that determines whether the current user or machine is being queried for activation status. This can be one of the following values.



#### DRM_ACTIVATE_MACHINE

The machine is being queried for activation status. The machine is considered activated if there is a valid lockbox for the logged-on user 
and a valid <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificates</a> in the per-user certificate store.

In Rights Management Services client 1.0, the machine is considered activated if there is a valid lockbox 
and a valid <a href="/previous-versions/windows/desktop/adrms_sdk/m-gly">machine certificate</a>.



#### DRM_ACTIVATE_GROUPIDENTITY

The current user is being queried for activation status.

The current user is considered activated if the certificate store of the current user has a <a href="/previous-versions/windows/desktop/adrms_sdk/r-gly">rights account certificate</a> issued to the specified group ID.

### -param pActServInfo [in]

This parameter is reserved and must be set to <b>NULL</b>.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

You can call <b>DRMIsActivated</b> to determine the current state of computer or user activation before calling any function that requires prior activation. If <b>DRMIsActivated</b> fails, call <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a>.

This function internally uses information contained in the client session. If the user ID associated with the client session does not match the ID of the logged–on user, this function will fail. For more information, see <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateclientsession">DRMCreateClientSession</a>.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/activating-a-computer">Activating a Computer</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/activating-a-user">Activating a User</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmactivate">DRMActivate</a>
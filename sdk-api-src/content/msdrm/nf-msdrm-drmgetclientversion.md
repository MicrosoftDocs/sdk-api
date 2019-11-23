---
UID: NF:msdrm.DRMGetClientVersion
title: DRMGetClientVersion function (msdrm.h)

description: Returns the version number of the Active Directory Rights Management Services client software and whether the hierarchy is for Production or Pre-production purposes.
old-location: rm\drmgetclientversion.htm
tech.root: AdRms_Sdk
ms.assetid: 51f15900-4d7a-414e-ab2a-9120cd23a03b

ms.date: 12/05/2018
ms.keywords: DRMGetClientVersion, DRMGetClientVersion function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetClientVersion, rm.drmgetclientversion
ms.topic: function
f1_keywords:
- msdrm/DRMGetClientVersion
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Msdrm.dll
api_name:
- DRMGetClientVersion
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
---

# DRMGetClientVersion function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetClientVersion</b> function returns the version number of the Active Directory Rights Management Services client software and whether the hierarchy is for Production or Pre-production purposes.


## -parameters




### -param pDRMClientVersionInfo [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drm_client_version_info">DRM_CLIENT_VERSION_INFO</a> structure that receives the version number of the Active Directory Rights Management Services client software and the hierarchy information, such as Production or Pre-production.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msdrmdefs/ns-msdrmdefs-drm_client_version_info">DRM_CLIENT_VERSION_INFO</a>
 

 


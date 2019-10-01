---
UID: NF:msdrm.DRMIsWindowProtected
title: DRMIsWindowProtected function (msdrm.h)
author: windows-sdk-content
description: Indicates whether a window is associated with a protected environment.
old-location: rm\drmiswindowprotected.htm
tech.root: AdRms_Sdk
ms.assetid: 5cd4b4fe-6941-441c-ac6c-9ec8d838598c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMIsWindowProtected, DRMIsWindowProtected function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMIsWindowProtected, rm.drmiswindowprotected
ms.topic: function
f1_keywords: 
 - "msdrm/DRMIsWindowProtected"
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
 - DRMIsWindowProtected
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DRMIsWindowProtected function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMIsWindowProtected</b> function indicates whether a window is associated with a protected environment.


## -parameters




### -param hwnd [in]

The window handle.


### -param pfProtected [out]

A pointer to a <b>BOOL</b> that indicates whether the window is associated with a protected environment.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>
 

 


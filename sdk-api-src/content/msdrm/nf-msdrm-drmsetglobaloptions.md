---
UID: NF:msdrm.DRMSetGlobalOptions
title: DRMSetGlobalOptions function
author: windows-sdk-content
description: Sets the transport protocol to a specified value and optionally specifies whether the server lockbox is used.
old-location: rm\drmsetglobaloptions.htm
tech.root: AdRms_Sdk
ms.assetid: fff0d503-e342-4f50-810c-bda4e9e14ad7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DRMSetGlobalOptions, DRMSetGlobalOptions function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMSetGlobalOptions, rm.drmsetglobaloptions
ms.topic: function
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
 - DRMSetGlobalOptions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMSetGlobalOptions function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMSetGlobalOptions</b> function sets the transport protocol to a specified value and optionally specifies whether the server lockbox is used.


## -parameters




### -param eGlobalOptions [in]

A value of the <a href="https://msdn.microsoft.com/57debd49-ec1e-432d-baac-2f828aeb4412">DRMGLOBALOPTIONS</a> enumeration that specifies the option to set.

Only one option can be specified in each call to <b>DRMSetGlobalOptions</b>. For example, if both WinHTTP and the server lockbox are required, you must call <b>DRMSetGlobalOptions</b> twice, once with <i>eGlobalOptions</i> set to <b>DRMGLOBALOPTIONS_USE_WINHTTP</b> and once with <i>eGlobalOptions</i> set to <b>DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR</b>.


### -param pvdata [in]

A pointer to a <b>void</b> value. This parameter is not currently used.


### -param dwlen [in]

The size, in bytes, of the <i>pvdata</i> buffer. This parameter is not currently used.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Applications cannot toggle between the WinHTTP and WinINet protocols.

WinINet does not support usage under the network service account. If an application will be run under the network service account, the application must specify the <b>DRMGLOBALOPTIONS_USE_WINHTTP</b> option.

An AD RMS-enabled server application should call the <b>DRMSetGlobalOptions</b> function prior to calling any other rights management functions. Calling <b>DRMSetGlobalOptions</b> after other rights management functions have been called will not change the type of lockbox or transport protocol in use.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/57debd49-ec1e-432d-baac-2f828aeb4412">DRMGLOBALOPTIONS</a>
 

 


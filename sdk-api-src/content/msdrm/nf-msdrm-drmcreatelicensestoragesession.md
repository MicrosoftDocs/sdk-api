---
UID: NF:msdrm.DRMCreateLicenseStorageSession
title: DRMCreateLicenseStorageSession function
author: windows-sdk-content
description: Creates a license storage session, which is needed to acquire or manipulate a license.
old-location: rm\drmcreatelicensestoragesession.htm
tech.root: AdRms_Sdk
ms.assetid: 6561b6df-373b-4bd3-9196-09ef945f8042
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DRMCreateLicenseStorageSession, DRMCreateLicenseStorageSession function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMCreateLicenseStorageSession, rm.drmcreatelicensestoragesession
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DRMCreateLicenseStorageSession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DRMCreateLicenseStorageSession
: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMCreateLicenseStorageSession function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMCreateLicenseStorageSession</b> function creates a license storage session, which is needed to acquire or manipulate a license.


## -parameters




### -param hEnv [in]

A handle to the AD RMS environment. This handle is obtained by using the <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a> function.


### -param hDefaultLibrary [in]

A handle to the default library. This handle is obtained by using the <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a> function.


### -param hClient [in]

A handle to a client session. This handle is obtained by using the <a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a> function.


### -param uFlags [in]

This parameter is reserved and must be set to zero.


### -param wszIssuanceLicense [in]

A pointer to a null-terminated Unicode string that contains a signed issuance license. The created license storage session is associated with this issuance license.


### -param phLicenseStorage [out]

A pointer to a handle that receives the license storage session handle. This handle must be passed to the <a href="https://msdn.microsoft.com/e948b31f-382c-4a32-8cc3-98df8c4a6db0">DRMCloseSession</a> function when the license storage session is no longer needed.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



A license storage session is used for acquiring, deleting, and enumerating licenses, among other uses. To actually bind to a license and exercise its rights, an application must use <a href="https://msdn.microsoft.com/102fa347-47be-4dc7-ba17-3f1ad3735b00">DRMCreateBoundLicense</a>.

The environment handle and default library handle are created by using <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>.

The handle returned in the <i>phLicenseStorage</i> parameter must be passed to the <a href="https://msdn.microsoft.com/e948b31f-382c-4a32-8cc3-98df8c4a6db0">DRMCloseSession</a> function when the license storage session is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/422f286c-edf6-488f-8776-359ab2695be3">DRMCloseHandle</a>



<a href="https://msdn.microsoft.com/4b8928a0-1d72-47ee-a357-47fb5777d60c">DRMCreateClientSession</a>



<a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>



<a href="https://msdn.microsoft.com/cc2b6faf-d768-4e6e-98e0-8d9022460582">Decryption_GetBoundLicense.cpp</a>
 

 


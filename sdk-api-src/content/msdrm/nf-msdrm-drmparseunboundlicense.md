---
UID: NF:msdrm.DRMParseUnboundLicense
title: DRMParseUnboundLicense function
author: windows-sdk-content
description: Creates a handle to an unbound license, to allow an application to navigate its objects and attributes.
old-location: rm\drmparseunboundlicense.htm
tech.root: AdRms_Sdk
ms.assetid: 2ae65ed2-7702-4e9b-b986-68b83ebe8bf5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DRMParseUnboundLicense, DRMParseUnboundLicense function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMParseUnboundLicense, rm.drmparseunboundlicense
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
 - DRMParseUnboundLicense
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DRMParseUnboundLicense
: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMParseUnboundLicense function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMParseUnboundLicense</b> function creates a handle to an unbound license, to allow an application to navigate its objects and attributes. For more information, see Remarks.


## -parameters




### -param wszCertificate [in]

The leaf certificate on the license to be examined, in plain text (not encoded).


### -param phQueryRoot [out]

Pointer to a handle to the root object of the license. Call <a href="https://msdn.microsoft.com/4902a6e2-e3b2-4f05-970c-aa4f80895762">DRMCloseQueryHandle</a> to close the handle.


## -returns



 If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function is for querying unbound end-user licenses, and also for obtaining license acquisition URLs from issuance licenses. The unbound end-user license retrieved by <a href="https://msdn.microsoft.com/7a7797f2-d219-4a17-ac3d-96134cd14a55">DRMEnumerateLicense</a> is a certificate chain. To properly query the unbound license itself, first call <a href="https://msdn.microsoft.com/893263cc-2647-4f62-b997-354ea976081f">DRMDeconstructCertificateChain</a> to obtain the first element of the chain (item zero), which is the actual license.

An application can navigate this interface using various <b>DRMGetUnboundLicense_xxx</b> functions (for unbound licenses). To examine bound licenses, use the <b>DRMGetBoundLicense_xxx</b> functions.

Both bound and unbound licenses can be examined. Whether you decide to use a bound or an unbound license depends on whether you need to exercise the rights or just examine the license. Bound licenses can exist only after a secure environment has been created using <a href="https://msdn.microsoft.com/b46277f4-e854-4590-847a-cf4f878bee70">DRMInitEnvironment</a>. Unbound licenses, however, do not require a secure environment.

The output of this function can be passed into one of the <b>DRMGetUnboundLicense_xxx</b> functions. The only object you can query for in an issuance license is g_wszQUERY_DISTRIBUTIONPOINT. The only attributes you can query for are g_wszQUERY_IDTYPE, g_wszQUERY_IDVALUE, g_wszQUERY_NAME, g_wszQUERY_ADDRESSTYPE, and g_wszQUERY_ADDRESSVALUE.

Call <a href="https://msdn.microsoft.com/4902a6e2-e3b2-4f05-970c-aa4f80895762">DRMCloseQueryHandle</a> to close the unbound license handle created by calling this function.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/7496380a-2848-4353-a672-27fc5a9eed92">Querying Licenses</a>
 

 


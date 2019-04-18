---
UID: NF:msdrm.DRMGetCertificateChainCount
title: DRMGetCertificateChainCount function (msdrm.h)
author: windows-sdk-content
description: Retrieves the number of certificates in a certificate chain.
old-location: rm\drmgetcertificatechaincount.htm
tech.root: AdRms_Sdk
ms.assetid: c19e7cfe-2a28-41d5-9075-3e159be1d9ab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DRMGetCertificateChainCount, DRMGetCertificateChainCount function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMGetCertificateChainCount, rm.drmgetcertificatechaincount
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
 - DRMGetCertificateChainCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
---

# DRMGetCertificateChainCount function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetCertificateChainCount</b> function retrieves the number of certificates in a certificate chain.


## -parameters




### -param wszChain [in]

The chain to count.


### -param pcCertCount [out]

The number of certificates in the chain.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function is used with <a href="https://msdn.microsoft.com/893263cc-2647-4f62-b997-354ea976081f">DRMDeconstructCertificateChain</a> to allow an application to loop through a certificate chain and retrieve individual certificates.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>
 

 


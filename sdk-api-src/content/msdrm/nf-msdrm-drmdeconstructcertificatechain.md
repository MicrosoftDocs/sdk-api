---
UID: NF:msdrm.DRMDeconstructCertificateChain
title: DRMDeconstructCertificateChain function
author: windows-sdk-content
description: Retrieves a specified certificate from a certificate chain.
old-location: rm\drmdeconstructcertificatechain.htm
old-project: adrms_sdk
ms.assetid: 893263cc-2647-4f62-b997-354ea976081f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DRMDeconstructCertificateChain, DRMDeconstructCertificateChain function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMDeconstructCertificateChain, rm.drmdeconstructcertificatechain
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_SELECTIONSTYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMDeconstructCertificateChain
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMDeconstructCertificateChain function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMDeconstructCertificateChain</b> function retrieves a specified certificate from a certificate chain.


## -parameters




### -param wszChain [in]

The certificate chain.


### -param iWhich [in]

A zero-based index specifying which certificate to retrieve.


### -param pcCert [in, out]

The length of the retrieved certificate, in characters, plus one for a null terminator.


### -param wszCert [out]

The certificate requested.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



This function allows an application to retrieve individual certificates from a chain. To determine the number of certificates available, use <a href="https://msdn.microsoft.com/c19e7cfe-2a28-41d5-9075-3e159be1d9ab">DRMGetCertificateChainCount</a>.

Memory allocation and deallocation for <i>wszCert</i> are handled by the caller. The <i>szChain</i> buffer length can be obtained from the <i>pcCert</i> parameter by calling this function with <b>NULL</b> in the <i>wszCert</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/cc2b6faf-d768-4e6e-98e0-8d9022460582">Decryption_GetBoundLicense.cpp</a>
 

 


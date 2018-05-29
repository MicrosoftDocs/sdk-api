---
UID: NF:msdrm.DRMConstructCertificateChain
title: DRMConstructCertificateChain function
author: windows-sdk-content
description: Builds a certificate chain from an arbitrary number of certificates.
old-location: rm\drmconstructcertificatechain.htm
old-project: AdRms_Sdk
ms.assetid: 27c2bf2e-54b1-4ed4-a754-e8b3b3bd58cb
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DRMConstructCertificateChain, DRMConstructCertificateChain function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMConstructCertificateChain, rm.drmconstructcertificatechain
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
req.typenames: TF_SELECTIONSTYLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdrm.dll
api_name:
-	DRMConstructCertificateChain
product: Windows
targetos: Windows
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# DRMConstructCertificateChain function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMConstructCertificateChain</b> function builds a certificate chain from an arbitrary number of certificates.


## -parameters




### -param cCertificates [in]

The number of certificates in the <i>rgwszCertificates</i> array.


### -param rgwszCertificates [in]

An array of null-terminated Unicode string pointers that contain the certificates to construct the chain from. The number of elements in this array is specified by the <i>cCertificates</i> parameter.


### -param pcChain [in, out]

A pointer to a <b>UINT</b> that, on input, contains the size, in Unicode characters, of the  <i>wszChain</i> string. This character count must include the terminating null character.

On output, this <b>UINT</b> receives the number of Unicode characters copied into the buffer, including the terminating null character.


### -param wszChain [out]

A pointer to a null-terminated Unicode string that receives the constructed chain.

To determine the required size for this buffer, call this function with <b>NULL</b> for the <i>wszChain</i> parameter. The required number of Unicode characters, including the terminating null character, will be returned in the <i>pcChain</i> parameter.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



Memory allocation and deallocation for the chain are handled by the caller. To determine the required size for the <i>wszChain</i> buffer, call this function with <b>NULL</b> for the <i>wszChain</i> parameter. The required number of Unicode characters, including the terminating null character, will be returned in the <i>pcChain</i> parameter.

This function can be used to transform certificate chains that are returned by the AD RMS SOAP methods into certificate chains that can be used by AD RMS functions. For an example, see <a href="https://msdn.microsoft.com/cc2b6faf-d768-4e6e-98e0-8d9022460582">Decryption_GetBoundLicense.cpp</a>.




## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/cc2b6faf-d768-4e6e-98e0-8d9022460582">Decryption_GetBoundLicense.cpp</a>
 

 


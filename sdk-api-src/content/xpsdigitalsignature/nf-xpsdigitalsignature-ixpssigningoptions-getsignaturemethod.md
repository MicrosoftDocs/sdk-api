---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetSignatureMethod
title: IXpsSigningOptions::GetSignatureMethod
author: windows-sdk-content
description: Gets the signature method.
old-location: xps\ixpssigningoptions_getsignaturemethod.htm
old-project: printdocs
ms.assetid: ab01420f-c401-463a-a695-4594c1f579d3
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetSignatureMethod, GetSignatureMethod method [XPS Documents and Packaging], GetSignatureMethod method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetSignatureMethod method, IXpsSigningOptions.GetSignatureMethod, IXpsSigningOptions::GetSignatureMethod, xps.ixpssigningoptions_getsignaturemethod, xpsdigitalsignature/IXpsSigningOptions::GetSignatureMethod
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsdigitalsignature.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsDigitalSignature.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_SIGN_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSigningOptions.GetSignatureMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSigningOptions::GetSignatureMethod


## -description


Gets the signature method.


## -parameters




### -param signatureMethod [out, retval]

The signature method that is expressed as a URI. If no signature method has been set, a <b>NULL</b> pointer is returned.

The following signature methods have been tested in Windows 7:


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



A signature method must be set before signing.

When a new instance of this interface is returned by <a href="https://msdn.microsoft.com/0f64f46a-905a-48cf-9e7a-f6cc1b2d6450">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod properties are not valid; they must be initialized before the new interface can be used as a parameter of the <a href="https://msdn.microsoft.com/82a57ca8-edc7-4248-92d1-8092f6dce4f8">Sign</a> method.

This method allocates the memory used by the string that is returned in <i>signatureMethod</i>.  If <i>signatureMethod</i> is not <b>NULL</b>, use the <a href="https://msdn.microsoft.com/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function to free the memory.




## -see-also




<a href="https://msdn.microsoft.com/9a65f73d-6f8c-4271-a2d0-d91ad952f9c6">Cryptography Functions</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


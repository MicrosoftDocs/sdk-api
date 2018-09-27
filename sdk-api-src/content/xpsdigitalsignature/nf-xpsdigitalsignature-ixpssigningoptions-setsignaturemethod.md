---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetSignatureMethod
title: IXpsSigningOptions::SetSignatureMethod
author: windows-sdk-content
description: Sets the signature method.
old-location: xps\ixpssigningoptions_setsignaturemethod.htm
tech.root: printdocs
ms.assetid: 318f0e08-2384-4fab-a181-6ff3070ea21f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetSignatureMethod method, IXpsSigningOptions.SetSignatureMethod, IXpsSigningOptions::SetSignatureMethod, SetSignatureMethod, SetSignatureMethod method [XPS Documents and Packaging], SetSignatureMethod method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setsignaturemethod, xpsdigitalsignature/IXpsSigningOptions::SetSignatureMethod
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsdigitalsignature.h
api_name:
 - IXpsSigningOptions.SetSignatureMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSigningOptions::SetSignatureMethod


## -description


Sets the signature method.


## -parameters




### -param signatureMethod [in]

The signature method expressed as a URI.

This parameter must refer to a valid signature method. The following signature methods have been tested in Windows 7:


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The signature method must be set before signing.

When a new instance of this interface is returned by <a href="https://msdn.microsoft.com/0f64f46a-905a-48cf-9e7a-f6cc1b2d6450">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod properties are not initialized; they must be initialized before the new interface can be used as a parameter of the <a href="https://msdn.microsoft.com/82a57ca8-edc7-4248-92d1-8092f6dce4f8">Sign</a> method.

The URI in  <i>signatureMethod</i>  must be the URI of a valid signing algorithm, such as http://www.w3.org/2000/09/xmldsig#rsa-sha1, and it must be
    supported by the signing certificate.




## -see-also




<a href="https://msdn.microsoft.com/9a65f73d-6f8c-4271-a2d0-d91ad952f9c6">Cryptography Functions</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


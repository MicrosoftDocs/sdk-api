---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetDigestMethod
title: IXpsSigningOptions::SetDigestMethod
author: windows-sdk-content
description: Sets the URI of the digest method.
old-location: xps\ixpssigningoptions_setdigestmethod.htm
tech.root: printdocs
ms.assetid: d9f72cc4-38b2-4a91-8813-183483d47986
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetDigestMethod method, IXpsSigningOptions.SetDigestMethod, IXpsSigningOptions::SetDigestMethod, SetDigestMethod, SetDigestMethod method [XPS Documents and Packaging], SetDigestMethod method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setdigestmethod, xpsdigitalsignature/IXpsSigningOptions::SetDigestMethod
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
 - IXpsSigningOptions.SetDigestMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsdigitalsignature.h
: 
- IXpsSigningOptions.SetDigestMethod
: 
---

# IXpsSigningOptions::SetDigestMethod


## -description


Sets the URI of the digest method.


## -parameters




### -param digestMethod [in]

The URI of the digest method.

This parameter must refer to the URI of a valid digest method. The following digest methods have been tested in Windows 7:


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The digest method must be set before signing.

When a new instance of this interface is returned by <a href="https://msdn.microsoft.com/0f64f46a-905a-48cf-9e7a-f6cc1b2d6450">IXpsSignatureManager::CreateSigningOptions</a>, the SignatureMethod and  DigestMethod properties are not initialized. They must be initialized before the new interface can be used as a parameter of the <a href="https://msdn.microsoft.com/82a57ca8-edc7-4248-92d1-8092f6dce4f8">Sign</a> method.

Sets the string  that identifies the URI of the algorithm that is used to digest the parts, relationships, and signature references. The following is an example of a valid URI:   <a href="http://www.w3.org/2000/09/xmldsig">http://www.w3.org/2000/09/xmldsig#sha1</a>.

The signing certificate, signature method, 
    and digest method must be compatible with one another.




## -see-also




<a href="https://msdn.microsoft.com/9a65f73d-6f8c-4271-a2d0-d91ad952f9c6">Cryptography Functions</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


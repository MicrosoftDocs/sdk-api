---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetCertificateSet
title: IXpsSigningOptions::GetCertificateSet
author: windows-sdk-content
description: Gets an IOpcCertificateSet interface, which can be used to add additional certificates to the signature.
old-location: xps\ixpssigningoptions_getcertificateset.htm
old-project: printdocs
ms.assetid: 40e96263-03dd-4fbe-8383-0c0bf1abd8c4
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetCertificateSet, GetCertificateSet method [XPS Documents and Packaging], GetCertificateSet method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetCertificateSet method, IXpsSigningOptions.GetCertificateSet, IXpsSigningOptions::GetCertificateSet, xps.ixpssigningoptions_getcertificateset, xpsdigitalsignature/IXpsSigningOptions::GetCertificateSet
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
req.typenames: XPS_SIGN_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsdigitalsignature.h
api_name:
-	IXpsSigningOptions.GetCertificateSet
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSigningOptions::GetCertificateSet


## -description


Gets an <a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a> interface, which can be used to add additional certificates to the signature.


## -parameters




### -param certificateSet [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a> interface.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Calling this  method is optional and provides a way for an application to add  a signing certificate to the signature. The extra certificates in this set will be separate from   the signing certificate.




## -see-also




<a href="https://msdn.microsoft.com/0ac56b41-a120-4a9b-9bfa-afba1ba0f3b4">IOpcCertificateSet</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


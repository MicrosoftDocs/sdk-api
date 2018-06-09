---
UID: NF:xpsdigitalsignature.IXpsSignature.GetCustomReferenceEnumerator
title: IXpsSignature::GetCustomReferenceEnumerator
author: windows-sdk-content
description: Gets a pointer to an IOpcSignatureReferenceEnumerator interface, which enumerates the custom references of the signature.
old-location: xps\ixpssignature_getcustomreferenceenumerator.htm
old-project: printdocs
ms.assetid: bcdbd3e0-a19a-448c-92b7-71720eff3386
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetCustomReferenceEnumerator, GetCustomReferenceEnumerator method [XPS Documents and Packaging], GetCustomReferenceEnumerator method [XPS Documents and Packaging],IXpsSignature interface, IXpsSignature interface [XPS Documents and Packaging],GetCustomReferenceEnumerator method, IXpsSignature.GetCustomReferenceEnumerator, IXpsSignature::GetCustomReferenceEnumerator, xps.ixpssignature_getcustomreferenceenumerator, xpsdigitalsignature/IXpsSignature::GetCustomReferenceEnumerator
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
 - IXpsSignature.GetCustomReferenceEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignature::GetCustomReferenceEnumerator


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a> interface, which enumerates the custom references of the signature.


## -parameters




### -param customReferenceEnumerator [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a> interface, which enumerates the custom references of the signature.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cfa38ef6-9d96-4577-a3bf-518784d19ad8">IOpcDigitalSignature</a>



<a href="https://msdn.microsoft.com/1d0a14c6-826c-419f-9e94-d5929fdbae82">IOpcSignatureReferenceEnumerator</a>



<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/31283ebe-91f4-42be-9a9b-6fcd641dc356">IXpsSignatureManager</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/d20707b0-55ea-438a-8ce3-972c61678928">XPS Digital Signature API Errors</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


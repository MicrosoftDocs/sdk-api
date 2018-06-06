---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetSignaturePartName
title: IXpsSigningOptions::GetSignaturePartName
author: windows-sdk-content
description: Gets the part name of the document's signature part.
old-location: xps\ixpssigningoptions_getsignaturepartname.htm
old-project: printdocs
ms.assetid: 8c5dfbda-0ceb-4694-bc5d-7e16e6f6d3bc
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetSignaturePartName, GetSignaturePartName method [XPS Documents and Packaging], GetSignaturePartName method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetSignaturePartName method, IXpsSigningOptions.GetSignaturePartName, IXpsSigningOptions::GetSignaturePartName, xps.ixpssigningoptions_getsignaturepartname, xpsdigitalsignature/IXpsSigningOptions::GetSignaturePartName
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
 - IXpsSigningOptions.GetSignaturePartName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSigningOptions::GetSignaturePartName


## -description


Gets the part name of the document's signature part.


## -parameters




### -param signaturePartName [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name of the document's signature part.

If a signature part name has not been set, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


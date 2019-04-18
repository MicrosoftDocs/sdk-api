---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetSignaturePartName
title: IXpsSigningOptions::SetSignaturePartName (xpsdigitalsignature.h)
author: windows-sdk-content
description: Sets the part name of the document's signature part.
old-location: xps\ixpssigningoptions_setsignaturepartname.htm
tech.root: printdocs
ms.assetid: 24addd5c-09a5-4f1b-90eb-c398aa7dd9a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetSignaturePartName method, IXpsSigningOptions.SetSignaturePartName, IXpsSigningOptions::SetSignaturePartName, SetSignaturePartName, SetSignaturePartName method [XPS Documents and Packaging], SetSignaturePartName method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setsignaturepartname, xpsdigitalsignature/IXpsSigningOptions::SetSignaturePartName
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
 - IXpsSigningOptions.SetSignaturePartName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsSigningOptions::SetSignaturePartName


## -description


Sets the part name of the document's signature part.


## -parameters




### -param signaturePartName [in]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that contains the part name of the document's signature part.

If this parameter is <b>NULL</b>, this method will generate a random, unique part name for the signature part.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


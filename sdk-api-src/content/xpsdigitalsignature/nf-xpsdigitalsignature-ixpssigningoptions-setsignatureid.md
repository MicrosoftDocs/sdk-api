---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetSignatureId
title: IXpsSigningOptions::SetSignatureId
author: windows-sdk-content
description: Sets the value of the Id attribute of the Signature element.
old-location: xps\ixpssigningoptions_setsignatureid.htm
tech.root: printdocs
ms.assetid: 314199f2-15bc-4ede-b18c-96c1dbfe5367
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetSignatureId method, IXpsSigningOptions.SetSignatureId, IXpsSigningOptions::SetSignatureId, SetSignatureId, SetSignatureId method [XPS Documents and Packaging], SetSignatureId method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setsignatureid, xpsdigitalsignature/IXpsSigningOptions::SetSignatureId
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
 - IXpsSigningOptions.SetSignatureId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSigningOptions::SetSignatureId


## -description


Sets the value of the <b>Id</b> attribute of the <b>Signature</b> element.


## -parameters




### -param signatureId [in]

The string value to be set as the <b>Id</b> attribute of the <b>Signature</b> element.  If this parameter is <b>NULL</b>, the <b>Id</b> attribute is cleared.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


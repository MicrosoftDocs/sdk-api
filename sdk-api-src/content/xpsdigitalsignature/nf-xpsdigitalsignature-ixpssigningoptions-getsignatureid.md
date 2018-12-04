---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetSignatureId
title: IXpsSigningOptions::GetSignatureId
author: windows-sdk-content
description: Gets the value of the Id attribute of the Signature element.
old-location: xps\ixpssigningoptions_getsignatureid.htm
tech.root: printdocs
ms.assetid: ebcb9f75-c9da-4559-9a9f-915b166801bf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetSignatureId, GetSignatureId method [XPS Documents and Packaging], GetSignatureId method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetSignatureId method, IXpsSigningOptions.GetSignatureId, IXpsSigningOptions::GetSignatureId, xps.ixpssigningoptions_getsignatureid, xpsdigitalsignature/IXpsSigningOptions::GetSignatureId
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
 - IXpsSigningOptions.GetSignatureId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSigningOptions::GetSignatureId


## -description


Gets the value of the <b>Id</b> attribute of the <b>Signature</b> element.


## -parameters




### -param signatureId [out, retval]

The value of the <b>Id</b> attribute of the <b>Signature</b> element. If  the <b>Id</b> attribute is not present, the method returns an empty string.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method allocates the memory used by the string that is returned in <i>signatureId</i>.  If <i>signatureId</i> is not <b>NULL</b>, use the <a href="_com_CoTaskMemFree">CoTaskMemFree</a> function to free the memory.

The default value of the signature ID is an empty string.




## -see-also




<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


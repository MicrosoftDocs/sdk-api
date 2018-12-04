---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.SetPolicy
title: IXpsSigningOptions::SetPolicy
author: windows-sdk-content
description: Sets the XPS_SIGN_POLICY value that represents the signing policy.
old-location: xps\ixpssigningoptions_setpolicy.htm
tech.root: printdocs
ms.assetid: 6e1738b3-f1ce-407e-bbaa-7f4c57e30028
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IXpsSigningOptions interface [XPS Documents and Packaging],SetPolicy method, IXpsSigningOptions.SetPolicy, IXpsSigningOptions::SetPolicy, SetPolicy, SetPolicy method [XPS Documents and Packaging], SetPolicy method [XPS Documents and Packaging],IXpsSigningOptions interface, xps.ixpssigningoptions_setpolicy, xpsdigitalsignature/IXpsSigningOptions::SetPolicy
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
 - IXpsSigningOptions.SetPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSigningOptions::SetPolicy


## -description


Sets the <a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a> value that represents the signing policy.


## -parameters




### -param policy [in]

The logical <b>OR</b> of  the <a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a> values to be set as the signing policy.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If an <a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a> value is set and it does not have a  corresponding part in the package being signed, only the  relationship type will be signed.




## -see-also




<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/88191931-4d6f-4ef3-ba75-227f6d2c2b10">XPS_SIGN_POLICY</a>
 

 


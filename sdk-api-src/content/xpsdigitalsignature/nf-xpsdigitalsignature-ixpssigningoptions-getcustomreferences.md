---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetCustomReferences
title: IXpsSigningOptions::GetCustomReferences
author: windows-sdk-content
description: Gets a pointer to an IOpcSignatureReferenceSet interface, which contains a set of signature custom references.
old-location: xps\ixpssigningoptions_getcustomreferences.htm
old-project: printdocs
ms.assetid: 1a9ab939-4581-40a9-acd3-2afe02c5e201
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetCustomReferences, GetCustomReferences method [XPS Documents and Packaging], GetCustomReferences method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetCustomReferences method, IXpsSigningOptions.GetCustomReferences, IXpsSigningOptions::GetCustomReferences, xps.ixpssigningoptions_getcustomreferences, xpsdigitalsignature/IXpsSigningOptions::GetCustomReferences
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
 - IXpsSigningOptions.GetCustomReferences
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSigningOptions::GetCustomReferences


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a> interface, which contains a set of signature custom references.


## -parameters




### -param customReferenceSet [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a> interface, which contains a set of signature custom references.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The custom reference set that this method returns is empty. To add  a custom reference to this set, call the <a href="https://msdn.microsoft.com/5e943769-a043-4354-80e7-d471a1dbde7a">Create</a> method of the  interface that is returned in <i>customReferenceSet</i>.

If a custom object must be signed, a reference to  that object  must be added  to the custom object set. For information on adding custom references, refer to  <b>GetCustomReferences</b>.




## -see-also




<a href="https://msdn.microsoft.com/7955ac86-de6e-4911-a107-a1617c14e685">IOpcSignatureReferenceSet</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


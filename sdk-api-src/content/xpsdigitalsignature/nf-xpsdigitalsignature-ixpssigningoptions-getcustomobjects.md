---
UID: NF:xpsdigitalsignature.IXpsSigningOptions.GetCustomObjects
title: IXpsSigningOptions::GetCustomObjects
author: windows-sdk-content
description: Gets a pointer to an IOpcSignatureCustomObjectSet interface that contains a set of signature custom objects.
old-location: xps\ixpssigningoptions_getcustomobjects.htm
tech.root: printdocs
ms.assetid: 17a3f913-57f2-40e1-b886-6cefb9e42a83
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetCustomObjects, GetCustomObjects method [XPS Documents and Packaging], GetCustomObjects method [XPS Documents and Packaging],IXpsSigningOptions interface, IXpsSigningOptions interface [XPS Documents and Packaging],GetCustomObjects method, IXpsSigningOptions.GetCustomObjects, IXpsSigningOptions::GetCustomObjects, xps.ixpssigningoptions_getcustomobjects, xpsdigitalsignature/IXpsSigningOptions::GetCustomObjects
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
 - IXpsSigningOptions.GetCustomObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSigningOptions::GetCustomObjects


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a> interface that contains a set of signature custom objects.


## -parameters




### -param customObjectSet [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a> interface that contains a set of signature custom objects.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The custom object set that this method returns is empty. To add  a custom object to this set, call the <a href="https://msdn.microsoft.com/93bf4509-900c-42bc-9834-c8a33cfe7e65">Create</a> method of the  interface that is returned in <i>customObjectSet</i>.

If a custom object must be signed, a reference to  that object  must be added  to the custom object set. For information on adding custom references, refer to  <a href="https://msdn.microsoft.com/1a9ab939-4581-40a9-acd3-2afe02c5e201">GetCustomReferences</a>.




## -see-also




<a href="https://msdn.microsoft.com/1a9ab939-4581-40a9-acd3-2afe02c5e201">GetCustomReferences</a>



<a href="https://msdn.microsoft.com/eb2a561d-2723-45dc-98a6-ecf11101016b">IOpcSignatureCustomObjectSet</a>



<a href="https://msdn.microsoft.com/5fb66c8f-2eb2-48c3-8e6f-04a1c509f6ec">IOpcSigningOptions</a>



<a href="https://msdn.microsoft.com/71b9b348-1078-4f55-a071-e5e2f273f85c">IXpsSigningOptions</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


---
UID: NF:xpsdigitalsignature.IXpsSignatureBlockCollection.GetCount
title: IXpsSignatureBlockCollection::GetCount
author: windows-sdk-content
description: Gets the number of IXpsSignatureBlock interface pointers in the collection.
old-location: xps\ixpssignatureblockcollection_getcount.htm
tech.root: printdocs
ms.assetid: d748e974-7350-44cd-9599-111f402d20e2
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetCount, GetCount method [XPS Documents and Packaging], GetCount method [XPS Documents and Packaging],IXpsSignatureBlockCollection interface, IXpsSignatureBlockCollection interface [XPS Documents and Packaging],GetCount method, IXpsSignatureBlockCollection.GetCount, IXpsSignatureBlockCollection::GetCount, xps.ixpssignatureblockcollection_getcount, xpsdigitalsignature/IXpsSignatureBlockCollection::GetCount
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
 - IXpsSignatureBlockCollection.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureBlockCollection::GetCount


## -description


Gets the number of <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface pointers in the collection.


## -parameters




### -param count [out, retval]

The number of <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface pointers in the collection.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a>



<a href="https://msdn.microsoft.com/e8f7be84-389e-40cf-a093-83417ba184c7">IXpsSignatureBlockCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


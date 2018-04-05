---
UID: NF:xpsdigitalsignature.IXpsSignatureBlockCollection.RemoveAt
title: IXpsSignatureBlockCollection::RemoveAt method
author: windows-driver-content
description: Removes and releases an IXpsSignatureBlock interface pointer from a specified location in the collection.
old-location: xps\ixpssignatureblockcollection_removeat.htm
old-project: printdocs
ms.assetid: 895f6f0b-6259-4288-90be-659f1ca46d1a
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsSignatureBlockCollection, IXpsSignatureBlockCollection interface [XPS Documents and Packaging], RemoveAt method, IXpsSignatureBlockCollection::RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging], IXpsSignatureBlockCollection interface, RemoveAt,IXpsSignatureBlockCollection.RemoveAt, xps.ixpssignatureblockcollection_removeat, xpsdigitalsignature/IXpsSignatureBlockCollection::RemoveAt
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
req.typenames: XPS_SIGN_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsdigitalsignature.h
api_name:
-	IXpsSignatureBlockCollection.RemoveAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureBlockCollection::RemoveAt method


## -description


Removes and releases an <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface pointer from a specified location in the collection.


## -parameters




### -param index

The zero-based index in the collection from which  an <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> interface pointer is to be removed and released.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



From the location specified by <i>index</i>, this method releases the interface  referenced by an <a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a> pointer. The method then compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.  For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.

Removing a signature block from the collection removes from the package the    SignatureDefinitions part and relationship that correspond to that signature block. This removal breaks existing signatures. In addition, the SignatureDefinitions part name is removed from the list of required XPS parts, which prevents  new signatures from including the removed signature block.

An interface that has been removed from a collection is no longer valid. If an application retains a pointer to the interface and tries to call one of its methods,  the  method will return <b>XPS_E_OBJECT_DETACHED</b>.




## -see-also




<a href="https://msdn.microsoft.com/cb2b7fe2-f3d9-4542-958f-5412d2498a9f">IXpsSignatureBlock</a>



<a href="https://msdn.microsoft.com/e8f7be84-389e-40cf-a093-83417ba184c7">IXpsSignatureBlockCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


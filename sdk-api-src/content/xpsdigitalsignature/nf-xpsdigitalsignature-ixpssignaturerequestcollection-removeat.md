---
UID: NF:xpsdigitalsignature.IXpsSignatureRequestCollection.RemoveAt
title: IXpsSignatureRequestCollection::RemoveAt
author: windows-sdk-content
description: Removes and releases an IXpsSignatureRequest interface pointer from a specified location in the collection.
old-location: xps\ixpssignaturerequestcollection_removeat.htm
tech.root: printdocs
ms.assetid: 6149de80-d0ca-4b6b-a092-b1c30f313df5
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IXpsSignatureRequestCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsSignatureRequestCollection.RemoveAt, IXpsSignatureRequestCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsSignatureRequestCollection interface, xps.ixpssignaturerequestcollection_removeat, xpsdigitalsignature/IXpsSignatureRequestCollection::RemoveAt
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
 - IXpsSignatureRequestCollection.RemoveAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsSignatureRequestCollection::RemoveAt


## -description


Removes and releases an <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection from which  an <a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a> interface pointer is to be removed and released.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method releases the interface pointer from  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.

After the interface has been removed from a collection, it is no longer valid. If an application retains a pointer to the removed interface and tries to call one of the interface's methods,  the  method will return <b>E_UNEXPECTED</b>.




## -see-also




<a href="https://msdn.microsoft.com/5ece2402-ab0e-4695-b9d7-478a65199ec8">IXpsSignatureRequest</a>



<a href="https://msdn.microsoft.com/bb8279e1-a98b-4156-8b90-d9b69411bfa3">IXpsSignatureRequestCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


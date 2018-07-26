---
UID: NF:xpsdigitalsignature.IXpsSignatureCollection.RemoveAt
title: IXpsSignatureCollection::RemoveAt
author: windows-sdk-content
description: Removes and releases an IXpsSignature interface pointer from a specified location in the collection.
old-location: xps\ixpssignaturecollection_removeat.htm
old-project: printdocs
ms.assetid: 513fcb60-1c07-4748-847c-6ccc7be25fbd
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IXpsSignatureCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsSignatureCollection.RemoveAt, IXpsSignatureCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsSignatureCollection interface, xps.ixpssignaturecollection_removeat, xpsdigitalsignature/IXpsSignatureCollection::RemoveAt
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
 - IXpsSignatureCollection.RemoveAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsSignatureCollection::RemoveAt


## -description


Removes and releases an <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface pointer from a specified location in the collection.


## -parameters




### -param index

The zero-based index in the collection from which  an <a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a> interface pointer is to be removed and released.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method releases an interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

Once an interface has been removed from a collection, it is no longer valid. If an application retains a pointer to the interface that was removed and tries to call one of its methods,  the  method will return <b>E_UNEXPECTED</b>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/23e2f9bd-7b0b-46ef-8ce3-a0c63be554e5">IXpsSignature</a>



<a href="https://msdn.microsoft.com/b8c46cc0-e071-4016-b658-1a5cd554a4c9">IXpsSignatureCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


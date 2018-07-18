---
UID: NF:xpsobjectmodel.IXpsOMSignatureBlockResourceCollection.GetByPartName
title: IXpsOMSignatureBlockResourceCollection::GetByPartName
author: windows-sdk-content
description: Gets an IXpsOMSignatureBlockResource interface pointer from the collection by matching the interface's part name.
old-location: xps\ixpsomsignatureblockresourcecollection_getbypartname.htm
old-project: printdocs
ms.assetid: 38e6d6d9-0f31-45e9-8a19-1aae02dfafd3
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetByPartName, GetByPartName method [XPS Documents and Packaging], GetByPartName method [XPS Documents and Packaging],IXpsOMSignatureBlockResourceCollection interface, IXpsOMSignatureBlockResourceCollection interface [XPS Documents and Packaging],GetByPartName method, IXpsOMSignatureBlockResourceCollection.GetByPartName, IXpsOMSignatureBlockResourceCollection::GetByPartName, xps.ixpsomsignatureblockresourcecollection_getbypartname, xpsobjectmodel/IXpsOMSignatureBlockResourceCollection::GetByPartName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMSignatureBlockResourceCollection.GetByPartName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMSignatureBlockResourceCollection::GetByPartName


## -description


Gets an <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface pointer from the collection by matching the interface's part name.


## -parameters




### -param partName [in]

The part name of the <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface to be found in the collection.


### -param signatureBlockResource [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/f5052470-487d-4f47-8d42-70538a4a45a8">IXpsOMSignatureBlockResource</a> interface whose part name matches <i>partName</i>. If a matching interface is not found in the collection, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/681bdb9c-69dd-4bf6-a4b3-c490f7a0363e">IXpsOMSignatureBlockResourceCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


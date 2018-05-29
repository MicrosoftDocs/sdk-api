---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResourceCollection.GetByPartName
title: IXpsOMRemoteDictionaryResourceCollection::GetByPartName
author: windows-sdk-content
description: Gets an IXpsOMRemoteDictionaryResource interface pointer from the collection by matching the interface's part name.
old-location: xps\ixpsomremotedictionaryresourcecollection_getbypartname.htm
old-project: printdocs
ms.assetid: e90f23d9-c161-4b3c-a6bc-0059d2dfe5b5
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetByPartName, GetByPartName method [XPS Documents and Packaging], GetByPartName method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResourceCollection interface, IXpsOMRemoteDictionaryResourceCollection interface [XPS Documents and Packaging],GetByPartName method, IXpsOMRemoteDictionaryResourceCollection.GetByPartName, IXpsOMRemoteDictionaryResourceCollection::GetByPartName, xps.ixpsomremotedictionaryresourcecollection_getbypartname, xpsobjectmodel/IXpsOMRemoteDictionaryResourceCollection::GetByPartName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMRemoteDictionaryResourceCollection.GetByPartName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMRemoteDictionaryResourceCollection::GetByPartName


## -description


Gets an <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer from the collection by matching the interface's part name.


## -parameters




### -param partName [in]

The part name of the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface to be found in the collection.


### -param remoteDictionaryResource [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface whose part name matches <i>partName</i>.  If a matching interface is not found in the collection, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


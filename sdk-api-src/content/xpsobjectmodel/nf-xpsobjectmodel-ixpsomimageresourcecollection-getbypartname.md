---
UID: NF:xpsobjectmodel.IXpsOMImageResourceCollection.GetByPartName
title: IXpsOMImageResourceCollection::GetByPartName
author: windows-sdk-content
description: Gets an IXpsOMImageResource interface pointer from the collection by matching the interface's part name.
old-location: xps\ixpsomimageresourcecollection_getbypartname.htm
old-project: printdocs
ms.assetid: 559461b4-49c1-4dd9-a370-05bfc71b4f36
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetByPartName, GetByPartName method [XPS Documents and Packaging], GetByPartName method [XPS Documents and Packaging],IXpsOMImageResourceCollection interface, IXpsOMImageResourceCollection interface [XPS Documents and Packaging],GetByPartName method, IXpsOMImageResourceCollection.GetByPartName, IXpsOMImageResourceCollection::GetByPartName, xps.ixpsomimageresourcecollection_getbypartname, xpsobjectmodel/IXpsOMImageResourceCollection::GetByPartName
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
 - IXpsOMImageResourceCollection.GetByPartName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMImageResourceCollection::GetByPartName


## -description


Gets an <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface pointer from the collection by matching the interface's part name.


## -parameters




### -param partName [in]

The part name of the interface that is to be found in the collection.


### -param part [out, retval]

The <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface whose part name matches <i>partName</i>.  If a matching interface is not found in the collection, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a>



<a href="https://msdn.microsoft.com/aed8b23e-71fd-49e6-aae9-006a59e0111b">IXpsOMImageResourceCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


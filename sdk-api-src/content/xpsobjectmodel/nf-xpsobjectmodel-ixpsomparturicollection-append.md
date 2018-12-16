---
UID: NF:xpsobjectmodel.IXpsOMPartUriCollection.Append
title: IXpsOMPartUriCollection::Append
author: windows-sdk-content
description: Appends an IOpcPartUri interface to the end of the collection.
old-location: xps\ixpsomparturicollection_append.htm
tech.root: printdocs
ms.assetid: 53d450cf-3e31-4d17-99cc-0552df771024
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Append, Append method [XPS Documents and Packaging], Append method [XPS Documents and Packaging],IXpsOMPartUriCollection interface, IXpsOMPartUriCollection interface [XPS Documents and Packaging],Append method, IXpsOMPartUriCollection.Append, IXpsOMPartUriCollection::Append, xps.ixpsomparturicollection_append, xpsobjectmodel/IXpsOMPartUriCollection::Append
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPartUriCollection.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPartUriCollection::Append


## -description


Appends an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface to the end of the collection.


## -parameters




### -param partUri [in]

A pointer to the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface that is to be appended to the collection.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/05fe9700-19e6-4e63-9693-cfa4b019f643">IXpsOMPartUriCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


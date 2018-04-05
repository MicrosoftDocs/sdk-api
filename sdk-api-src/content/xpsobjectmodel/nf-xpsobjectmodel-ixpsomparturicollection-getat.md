---
UID: NF:xpsobjectmodel.IXpsOMPartUriCollection.GetAt
title: IXpsOMPartUriCollection::GetAt method
author: windows-driver-content
description: Gets an IOpcPartUri interface pointer from a specified location in the collection.
old-location: xps\ixpsomparturicollection_getat.htm
old-project: printdocs
ms.assetid: 9d7fcc13-13f5-494d-b6b2-d1180902ec08
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging], IXpsOMPartUriCollection interface, GetAt,IXpsOMPartUriCollection.GetAt, IXpsOMPartUriCollection, IXpsOMPartUriCollection interface [XPS Documents and Packaging], GetAt method, IXpsOMPartUriCollection::GetAt, xps.ixpsomparturicollection_getat, xpsobjectmodel/IXpsOMPartUriCollection::GetAt
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IXpsOMPartUriCollection.GetAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPartUriCollection::GetAt method


## -description


Gets an <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer to be obtained.


### -param partUri [out, retval]

The <a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/05fe9700-19e6-4e63-9693-cfa4b019f643">IXpsOMPartUriCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


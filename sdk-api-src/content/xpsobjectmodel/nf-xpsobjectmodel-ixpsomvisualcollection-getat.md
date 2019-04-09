---
UID: NF:xpsobjectmodel.IXpsOMVisualCollection.GetAt
title: IXpsOMVisualCollection::GetAt (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets an IXpsOMVisual interface pointer from a specified location in the collection.
old-location: xps\ixpsomvisualcollection_getat.htm
tech.root: printdocs
ms.assetid: 8bd54fab-64e8-42a5-ac9d-fa19328b1acb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMVisualCollection interface, IXpsOMVisualCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMVisualCollection.GetAt, IXpsOMVisualCollection::GetAt, xps.ixpsomvisualcollection_getat, xpsobjectmodel/IXpsOMVisualCollection::GetAt
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
 - IXpsOMVisualCollection.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisualCollection::GetAt


## -description


Gets an <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a> interface pointer to be obtained.


### -param object [out, retval]

The <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/f373b437-3973-40aa-9cac-a6b196a3e5d1">IXpsOMVisualCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


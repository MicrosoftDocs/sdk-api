---
UID: NF:xpsobjectmodel.IXpsOMGradientStopCollection.GetAt
title: IXpsOMGradientStopCollection::GetAt
author: windows-sdk-content
description: Gets an IXpsOMGradientStop interface pointer from a specified location in the collection.
old-location: xps\ixpsomgradientstopcollection_getat.htm
tech.root: printdocs
ms.assetid: 5e75d595-0124-4239-b53e-f1b8101d2dcf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetAt, GetAt method [XPS Documents and Packaging], GetAt method [XPS Documents and Packaging],IXpsOMGradientStopCollection interface, IXpsOMGradientStopCollection interface [XPS Documents and Packaging],GetAt method, IXpsOMGradientStopCollection.GetAt, IXpsOMGradientStopCollection::GetAt, xps.ixpsomgradientstopcollection_getat, xpsobjectmodel/IXpsOMGradientStopCollection::GetAt
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMGradientStopCollection.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMGradientStopCollection.GetAt
: 
---

# IXpsOMGradientStopCollection::GetAt


## -description


Gets an <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index of the <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface pointer to be obtained.


### -param stop [out, retval]

The <a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a> interface pointer at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>



<a href="https://msdn.microsoft.com/1f51f818-e9bb-4d88-9795-4e6890d24b8c">IXpsOMGradientStopCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


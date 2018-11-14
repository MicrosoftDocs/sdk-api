---
UID: NF:xpsobjectmodel.IXpsOMFontResourceCollection.RemoveAt
title: IXpsOMFontResourceCollection::RemoveAt
author: windows-sdk-content
description: Removes and releases an IXpsOMFontResource interface pointer from a specified location in the collection.
old-location: xps\ixpsomfontresourcecollection_removeat.htm
tech.root: printdocs
ms.assetid: adcb8673-47ab-4d2f-829f-49d78ab26273
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMFontResourceCollection interface [XPS Documents and Packaging],RemoveAt method, IXpsOMFontResourceCollection.RemoveAt, IXpsOMFontResourceCollection::RemoveAt, RemoveAt, RemoveAt method [XPS Documents and Packaging], RemoveAt method [XPS Documents and Packaging],IXpsOMFontResourceCollection interface, xps.ixpsomfontresourcecollection_removeat, xpsobjectmodel/IXpsOMFontResourceCollection::RemoveAt
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
 - IXpsOMFontResourceCollection.RemoveAt
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
- IXpsOMFontResourceCollection.RemoveAt
: 
---

# IXpsOMFontResourceCollection::RemoveAt


## -description


Removes and releases an <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface pointer from a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection from which  an <a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a> interface pointer is to be removed and released.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



This method releases the interface  referenced by the pointer at  the location specified by <i>index</i>. After releasing the interface, this method compacts the collection by   reducing by 1 the index of each pointer subsequent to <i>index</i>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd0ce1c0-1c04-46a8-9075-93de9b3e3062">IXpsOMFontResource</a>



<a href="https://msdn.microsoft.com/71153c4c-631b-4f7a-9dd5-8537dcaca150">IXpsOMFontResourceCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


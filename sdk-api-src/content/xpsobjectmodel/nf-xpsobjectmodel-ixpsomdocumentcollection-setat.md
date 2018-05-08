---
UID: NF:xpsobjectmodel.IXpsOMDocumentCollection.SetAt
title: IXpsOMDocumentCollection::SetAt
author: windows-driver-content
description: Replaces an IXpsOMDocument interface pointer at a specified location in the collection.
old-location: xps\ixpsomdocumentcollection_setat.htm
old-project: printdocs
ms.assetid: 71279337-33ec-4ed3-8c87-9c9b6844d26b
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMDocumentCollection interface [XPS Documents and Packaging],SetAt method, IXpsOMDocumentCollection.SetAt, IXpsOMDocumentCollection::SetAt, SetAt, SetAt method [XPS Documents and Packaging], SetAt method [XPS Documents and Packaging],IXpsOMDocumentCollection interface, xps.ixpsomdocumentcollection_setat, xpsobjectmodel/IXpsOMDocumentCollection::SetAt
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
-	IXpsOMDocumentCollection.SetAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocumentCollection::SetAt


## -description


Replaces an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer at a specified location in the collection.


## -parameters




### -param index [in]

The zero-based index in the collection where an <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer is to be replaced.


### -param document [in]

The <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface pointer that will replace current contents at the location specified by <i>index</i>.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



At the location specified by <i>index</i>, this method releases the <a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a> interface referenced by the existing pointer, then writes the pointer that is passed in <i>document</i>.

For more information about the collection methods, see  <a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a>



<a href="https://msdn.microsoft.com/4f3acae9-10a0-47ff-9170-a40abe230580">IXpsOMDocumentCollection</a>



<a href="https://msdn.microsoft.com/6ea311c0-a155-47de-ad40-62b0cbeb6e8f">Working with XPS OM Collection Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


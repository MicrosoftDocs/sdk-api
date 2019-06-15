---
UID: NF:xpsobjectmodel.IXpsOMDashCollection.Append
title: IXpsOMDashCollection::Append (xpsobjectmodel.h)
author: windows-sdk-content
description: Appends an XPS_DASH structure to the end of the collection.
old-location: xps\ixpsomdashcollection_append.htm
tech.root: printdocs
ms.assetid: e8d2baf5-e36e-4363-bde6-1731c97e702f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Append, Append method [XPS Documents and Packaging], Append method [XPS Documents and Packaging],IXpsOMDashCollection interface, IXpsOMDashCollection interface [XPS Documents and Packaging],Append method, IXpsOMDashCollection.Append, IXpsOMDashCollection::Append, xps.ixpsomdashcollection_append, xpsobjectmodel/IXpsOMDashCollection::Append
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
 - IXpsOMDashCollection.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMDashCollection::Append


## -description


Appends an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/ns-xpsobjectmodel-__midl___midl_itf_xpsobjectmodel_0000_0000_0020">XPS_DASH</a> structure to the end of the collection.


## -parameters




### -param dash [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/ns-xpsobjectmodel-__midl___midl_itf_xpsobjectmodel_0000_0000_0020">XPS_DASH</a> structure that is to be appended  to the collection.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The figure that follows illustrates how the collection is changed by the <b>Append</b> method.

<img alt="A figure that shows how Append adds an entry to the dash collection" src="../images/dashcollection_append.png"/>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection">IXpsOMDashCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/ns-xpsobjectmodel-__midl___midl_itf_xpsobjectmodel_0000_0000_0020">XPS_DASH</a>
 

 


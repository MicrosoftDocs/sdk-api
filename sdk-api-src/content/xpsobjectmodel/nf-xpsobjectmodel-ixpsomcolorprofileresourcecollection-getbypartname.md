---
UID: NF:xpsobjectmodel.IXpsOMColorProfileResourceCollection.GetByPartName
title: IXpsOMColorProfileResourceCollection::GetByPartName (xpsobjectmodel.h)
description: Gets an IXpsOMColorProfileResource interface pointer from the collection by matching the interface's part name.
old-location: xps\ixpsomcolorprofileresourcecollection_getbypartname.htm
tech.root: printdocs
ms.assetid: 9c9dc7d0-af93-4bf3-b8ba-799c1e4bb273
ms.date: 12/05/2018
ms.keywords: GetByPartName, GetByPartName method [XPS Documents and Packaging], GetByPartName method [XPS Documents and Packaging],IXpsOMColorProfileResourceCollection interface, IXpsOMColorProfileResourceCollection interface [XPS Documents and Packaging],GetByPartName method, IXpsOMColorProfileResourceCollection.GetByPartName, IXpsOMColorProfileResourceCollection::GetByPartName, xps.ixpsomcolorprofileresourcecollection_getbypartname, xpsobjectmodel/IXpsOMColorProfileResourceCollection::GetByPartName
f1_keywords:
- xpsobjectmodel/IXpsOMColorProfileResourceCollection.GetByPartName
dev_langs:
- c++
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
- IXpsOMColorProfileResourceCollection.GetByPartName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMColorProfileResourceCollection::GetByPartName


## -description


Gets an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface pointer from the collection by matching the interface's part name.


## -parameters




### -param partName [in]

The part name of the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface to be found in  the collection.


### -param part [out, retval]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface whose part name  matches <i>partName</i>. If a matching interface is not found in the collection, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi">IOpcPartUri</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection">IXpsOMColorProfileResourceCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


---
UID: NN:xpsobjectmodel.IXpsOMRemoteDictionaryResource
title: IXpsOMRemoteDictionaryResource (xpsobjectmodel.h)
author: windows-sdk-content
description: Provides an interface that enables pages in an XPS package to share resources.
old-location: xps\ixpsomremotedictionaryresource.htm
tech.root: printdocs
ms.assetid: dd757856-f16e-46ad-b865-8203c3428372
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMRemoteDictionaryResource, IXpsOMRemoteDictionaryResource interface [XPS Documents and Packaging], IXpsOMRemoteDictionaryResource interface [XPS Documents and Packaging],described, xps.ixpsomremotedictionaryresource, xpsobjectmodel/IXpsOMRemoteDictionaryResource
ms.topic: interface
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
 - IXpsOMRemoteDictionaryResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMRemoteDictionaryResource interface


## -description


Provides an interface that enables pages in an XPS package to  share resources.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMRemoteDictionaryResource</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>. <b>IXpsOMRemoteDictionaryResource</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMRemoteDictionaryResource</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomremotedictionaryresource-getdictionary">GetDictionary</a>
</td>
<td align="left" width="63%">
Gets a pointer to the  <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface  of the remote dictionary that is associated with this resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomremotedictionaryresource-setdictionary">SetDictionary</a>
</td>
<td align="left" width="63%">
Sets a   pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a> interface of the remote dictionary that is to be associated with this resource.
            

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createremotedictionaryresource">IXpsOMObjectFactory::CreateRemoteDictionaryResource</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createremotedictionaryresourcefromstream">IXpsOMObjectFactory::CreateRemoteDictionaryResourceFromStream</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372762(v=vs.85)">IXpsOMResource</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd316980(v=vs.85)">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


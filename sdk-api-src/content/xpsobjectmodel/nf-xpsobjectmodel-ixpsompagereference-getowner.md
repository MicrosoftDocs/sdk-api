---
UID: NF:xpsobjectmodel.IXpsOMPageReference.GetOwner
title: IXpsOMPageReference::GetOwner (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets a pointer to the IXpsOMDocument interface that contains the page reference.
old-location: xps\ixpsompagereference_getowner.htm
tech.root: printdocs
ms.assetid: 1229972d-ae0f-41db-aafb-99d9647360e1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],GetOwner method, IXpsOMPageReference.GetOwner, IXpsOMPageReference::GetOwner, xps.ixpsompagereference_getowner, xpsobjectmodel/IXpsOMPageReference::GetOwner
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMPageReference.GetOwner"
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
 - IXpsOMPageReference.GetOwner
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMPageReference::GetOwner


## -description


Gets a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface that contains the page reference.


## -parameters




### -param document [out, retval]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a> interface that contains the page reference. If the page reference does not have an owner, a <b>NULL</b> pointer is returned.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>document</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument">IXpsOMDocument</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference">IXpsOMPageReference</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


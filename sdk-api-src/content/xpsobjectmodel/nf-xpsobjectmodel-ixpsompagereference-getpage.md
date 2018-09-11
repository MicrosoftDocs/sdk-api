---
UID: NF:xpsobjectmodel.IXpsOMPageReference.GetPage
title: IXpsOMPageReference::GetPage
author: windows-sdk-content
description: Gets a pointer to the IXpsOMPage interface that contains the page.
old-location: xps\ixpsompagereference_getpage.htm
tech.root: printdocs
ms.assetid: 0004217f-f379-4175-bbce-eea93d96f37f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetPage, GetPage method [XPS Documents and Packaging], GetPage method [XPS Documents and Packaging],IXpsOMPageReference interface, IXpsOMPageReference interface [XPS Documents and Packaging],GetPage method, IXpsOMPageReference.GetPage, IXpsOMPageReference::GetPage, xps.ixpsompagereference_getpage, xpsobjectmodel/IXpsOMPageReference::GetPage
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
 - IXpsOMPageReference.GetPage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPageReference::GetPage


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface that contains the page.


## -parameters




### -param page [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a> interface of the page. If a page has not been set, a <b>NULL</b> pointer is returned.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
 

This method calls the <a href="https://msdn.microsoft.com/77df9cb2-757e-4b07-9c1c-73af0df4702f">Packaging</a> API. For information about the Packaging API return values, see <a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>.




## -remarks



If a page has not been set but the <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface that contains the page's reference has loaded from an XPS package, this method will load and return the page. If a page has not been set and the <b>IXpsOMPackage</b> interface that contains this page reference has not loaded from an XPS package, a <b>NULL</b> pointer will be returned.

Depending on the page's contents, this call might take some time to return and it might also  cause unexpected changes in  other objects in the document tree. For example, if the page has remote resource dictionary references, the remote resource dictionary might get modified.




## -see-also




<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/430b9169-7fc5-493d-85a8-dddf46dfef8f">IXpsOMPageReference::DiscardPage</a>



<a href="https://msdn.microsoft.com/7d1381ad-6ac8-4ea4-99a2-8bc5d95773c7">IXpsOMPageReference::SetPage</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


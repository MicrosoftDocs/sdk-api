---
UID: NF:xpsobjectmodel.IXpsOMPage.GetName
title: IXpsOMPage::GetName (xpsobjectmodel.h)
description: Gets the Name property of the page.
helpviewer_keywords: ["GetName","GetName method [XPS Documents and Packaging]","GetName method [XPS Documents and Packaging]","IXpsOMPage interface","IXpsOMPage interface [XPS Documents and Packaging]","GetName method","IXpsOMPage.GetName","IXpsOMPage::GetName","xps.ixpsompage_getname","xpsobjectmodel/IXpsOMPage::GetName"]
old-location: xps\ixpsompage_getname.htm
tech.root: xps
ms.assetid: 0c133dce-3a5a-4d7f-af83-2e185450c207
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [XPS Documents and Packaging], GetName method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetName method, IXpsOMPage.GetName, IXpsOMPage::GetName, xps.ixpsompage_getname, xpsobjectmodel/IXpsOMPage::GetName
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMPage::GetName
 - xpsobjectmodel/IXpsOMPage::GetName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPage.GetName
---

# IXpsOMPage::GetName


## -description

Gets the <b>Name</b> property of the page.

## -parameters

### -param name [out, retval]

The <b>Name</b> property of the page. A <b>NULL</b> pointer is returned if  the <b>Name</b> property has not been set.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>name</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method allocates the memory used by the string that is returned in <i>name</i>.  If <i>name</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage">IXpsOMPage</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
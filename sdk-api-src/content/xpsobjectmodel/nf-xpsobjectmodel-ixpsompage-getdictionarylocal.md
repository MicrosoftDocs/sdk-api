---
UID: NF:xpsobjectmodel.IXpsOMPage.GetDictionaryLocal
title: IXpsOMPage::GetDictionaryLocal
author: windows-sdk-content
description: Gets a pointer to the IXpsOMDictionary interface of the local, unshared dictionary that is associated with this page.
old-location: xps\ixpsompage_getdictionarylocal.htm
tech.root: printdocs
ms.assetid: 1eece7d5-2f2d-4fae-a2f4-8e52236f57c4
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetDictionaryLocal, GetDictionaryLocal method [XPS Documents and Packaging], GetDictionaryLocal method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetDictionaryLocal method, IXpsOMPage.GetDictionaryLocal, IXpsOMPage::GetDictionaryLocal, xps.ixpsompage_getdictionarylocal, xpsobjectmodel/IXpsOMPage::GetDictionaryLocal
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
 - IXpsOMPage.GetDictionaryLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPage::GetDictionaryLocal


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the local, unshared dictionary that is associated with this page.


## -parameters




### -param resourceDictionary [out, retval]

A pointer to the  <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the local, unshared dictionary that is associated with this page. If no <b>IXpsOMDictionary</b> interface pointer has been set or if a remote dictionary resource has been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>resourceDictionary</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a>


</td>
<td>
The local dictionary resource that is set by <a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/e424c70e-289c-4519-8b20-5fb98d46bf34">SetDictionaryResource</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a> nor <a href="https://msdn.microsoft.com/e424c70e-289c-4519-8b20-5fb98d46bf34">SetDictionaryResource</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 


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
<i>resourceDictionary</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


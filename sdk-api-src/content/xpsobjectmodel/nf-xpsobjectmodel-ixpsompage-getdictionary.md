---
UID: NF:xpsobjectmodel.IXpsOMPage.GetDictionary
title: IXpsOMPage::GetDictionary
author: windows-sdk-content
description: Gets a pointer to the resolved IXpsOMDictionary interface that is associated with this page.
old-location: xps\ixpsompage_getdictionary.htm
old-project: printdocs
ms.assetid: e842c828-6e8c-4190-b845-8c8a26af1579
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetDictionary, GetDictionary method [XPS Documents and Packaging], GetDictionary method [XPS Documents and Packaging],IXpsOMPage interface, IXpsOMPage interface [XPS Documents and Packaging],GetDictionary method, IXpsOMPage.GetDictionary, IXpsOMPage::GetDictionary, xps.ixpsompage_getdictionary, xpsobjectmodel/IXpsOMPage::GetDictionary
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMPage.GetDictionary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPage::GetDictionary


## -description


Gets a pointer to the resolved <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface that is associated with this page.


## -parameters




### -param resourceDictionary [out, retval]

A pointer to the resolved <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface that is associated with this page.

The value that is returned in this parameter depends on which method has most recently been called to set the dictionary.

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
The shared dictionary in the dictionary resource that is set by <a href="https://msdn.microsoft.com/e424c70e-289c-4519-8b20-5fb98d46bf34">SetDictionaryResource</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_INVALID_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name set by  <a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a> references an object that is not a brush.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the lookup value.

No object could be found with a key name that matched the value passed in <i>lookup</i>.

</td>
</tr>
</table>
 




## -remarks



Whether the dictionary is local or is contained within a remote dictionary resource, this method returns an <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface pointer. <a href="https://msdn.microsoft.com/3570ad03-2b68-4294-b236-86bd372876a2">GetOwner</a> determines whether the dictionary  is remote.

If a page contains a remote dictionary, <b>GetDictionary</b> will deserialize the dictionary. If the page contains a remote dictionary that is not valid, <b>GetDictionary</b> might return a deserialization error code.

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a>



<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


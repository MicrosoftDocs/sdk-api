---
UID: NF:xpsobjectmodel.IXpsOMPage.SetDictionaryResource
title: IXpsOMPage::SetDictionaryResource
author: windows-sdk-content
description: Sets the IXpsOMRemoteDictionaryResource interface pointer of the page's remote dictionary resource.
old-location: xps\ixpsompage_setdictionaryresource.htm
old-project: printdocs
ms.assetid: e424c70e-289c-4519-8b20-5fb98d46bf34
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetDictionaryResource method, IXpsOMPage.SetDictionaryResource, IXpsOMPage::SetDictionaryResource, SetDictionaryResource, SetDictionaryResource method [XPS Documents and Packaging], SetDictionaryResource method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setdictionaryresource, xpsobjectmodel/IXpsOMPage::SetDictionaryResource
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMPage.SetDictionaryResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPage::SetDictionaryResource


## -description


Sets the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer of the page's remote dictionary resource.


## -parameters




### -param remoteDictionaryResource [in]

The <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer to be set for the page. A <b>NULL</b> value releases the previously assigned dictionary resource.


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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>remoteDictionaryResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



Setting this value will cause <a href="https://msdn.microsoft.com/1eece7d5-2f2d-4fae-a2f4-8e52236f57c4">GetDictionaryLocal</a> to return <b>NULL</b>.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>resourceDictionary</i> by <a href="https://msdn.microsoft.com/e842c828-6e8c-4190-b845-8c8a26af1579">GetDictionary</a>
</th>
<th>Object that is returned in <i>resourceDictionary</i>  by <a href="https://msdn.microsoft.com/1eece7d5-2f2d-4fae-a2f4-8e52236f57c4">GetDictionaryLocal</a>
</th>
<th>Object that is returned in <i>remoteDictionaryResource</i>   by <a href="https://msdn.microsoft.com/12313d19-e6f1-4ec3-9702-2a403087763a">GetDictionaryResource</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a>


</td>
<td>
The local dictionary resource that is set by <a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a>.

</td>
<td>
The local dictionary resource that is set by <a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a>.

</td>
<td>
<b>NULL</b> pointer. 

</td>
</tr>
<tr>
<td>
<b>SetDictionaryResource</b> (this method)

</td>
<td>
The shared dictionary in the dictionary resource that is set by <b>SetDictionaryResource</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The remote dictionary resource that is set by <b>SetDictionaryResource</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/d950a21a-0afe-410a-9f2c-32847c35471e">SetDictionaryLocal</a> nor <b>SetDictionaryResource</b> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


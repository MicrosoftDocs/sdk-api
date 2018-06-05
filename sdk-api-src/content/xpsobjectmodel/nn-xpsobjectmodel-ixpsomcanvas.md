---
UID: NN:xpsobjectmodel.IXpsOMCanvas
title: IXpsOMCanvas
author: windows-sdk-content
description: A group of visual elements and related properties.
old-location: xps\ixpsomcanvas.htm
old-project: printdocs
ms.assetid: 3cb0e1b3-88a8-4724-a3c5-0df416294e62
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMCanvas, IXpsOMCanvas interface [XPS Documents and Packaging], IXpsOMCanvas interface [XPS Documents and Packaging],described, xps.ixpsomcanvas, xpsobjectmodel/IXpsOMCanvas
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMCanvas
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCanvas interface


## -description


A group of visual elements and related properties.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMCanvas</b> interface inherits from <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>. <b>IXpsOMCanvas</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMCanvas</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a deep copy of the interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af2ea930-973e-4921-a6c8-192fa5bf4f9b">GetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Gets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c07f394d-b10f-45c1-b8b7-cd466507967b">GetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Gets a short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f32b534e-92bf-4e80-9ac1-b2577e076bed">GetDictionary</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the resolved <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the dictionary associated with the canvas.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5578ae0f-4da7-4d9f-9133-fbe501ff66a1">GetDictionaryLocal</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the local, unshared dictionary.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96fa8c03-ce00-4d10-8a88-228600fdcae7">GetDictionaryResource</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface of the remote dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d3f0660-227a-4b0f-bd41-112bd89e4605">GetUseAliasedEdgeMode</a>
</td>
<td align="left" width="63%">
Gets a Boolean value that determines whether the edges of the objects in the canvas are to be rendered using the aliased edge mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67f42c32-f9d2-4d64-a8e1-b18a0d5f55fa">GetVisuals</a>
</td>
<td align="left" width="63%">

              Gets a pointer to an <a href="https://msdn.microsoft.com/f373b437-3973-40aa-9cac-a6b196a3e5d1">IXpsOMVisualCollection</a> interface that contains a collection of the visual objects in the canvas.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b9da720-2823-4749-b881-3b9cd5c303a4">SetAccessibilityLongDescription</a>
</td>
<td align="left" width="63%">
Sets the long (detailed) textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0968e378-99eb-470c-9bf0-51f65906b07b">SetAccessibilityShortDescription</a>
</td>
<td align="left" width="63%">
Sets the short textual description of the object's contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface pointer of the local, unshared dictionary.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer of the remote dictionary resource.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a16b10fe-5065-4044-b632-452a79f61e90">SetUseAliasedEdgeMode</a>
</td>
<td align="left" width="63%">
Sets the value that determines whether the edges of objects in this canvas will be rendered using the aliased edge mode.

</td>
</tr>
</table> 


## -remarks



The code example that follows illustrates how to create an instance of  this interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMCanvas    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreateCanvas (&amp;newInterface);
    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface-&gt;Release();
    }
    xpsFactory-&gt;Release();
}
else
{
    // evaluate HRESULT error returned in hr
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1ee3a80d-f6d8-45ba-8178-e3870404698a">IXpsOMObjectFactory::CreateCanvas</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


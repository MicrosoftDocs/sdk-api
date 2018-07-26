---
UID: NN:xpsobjectmodel.IXpsOMPackage
title: IXpsOMPackage
author: windows-sdk-content
description: Provides the top-level entry into the XPS object model tree.
old-location: xps\ixpsompackage.htm
old-project: printdocs
ms.assetid: 7b0a36d6-1af1-4c2c-af14-d6139e9115c3
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IXpsOMPackage, IXpsOMPackage interface [XPS Documents and Packaging], IXpsOMPackage interface [XPS Documents and Packaging],described, xps.ixpsompackage, xpsobjectmodel/IXpsOMPackage
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMPackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPackage interface


## -description


Provides the top-level entry into the XPS object model tree.

 Although this interface does not correspond to any XPS markup, it does correspond to the XPS document, and it is required to save the components of an XPS object model tree as an XPS document.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IXpsOMPackage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IXpsOMPackage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IXpsOMPackage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebe5c8a2-2d6a-4a86-8bf3-1fec1dec68d0">GetCoreProperties</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the  <a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a> interface of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1c60001-0a0c-4ff9-bb17-fef3e47b16a6">GetDiscardControlPartName</a>
</td>
<td align="left" width="63%">
Gets the name of the discard control part in the XPS package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30789376-1ac8-41ae-9c4d-e3d2d0715016">GetDocumentSequence</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the  <a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a> interface that contains the document sequence of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44a692a4-de5d-4fa9-89e2-ad969042797a">GetThumbnailResource</a>
</td>
<td align="left" width="63%">

              Gets a pointer to the <a href="https://msdn.microsoft.com/89a1530e-fa87-45bf-a1da-c8656ec09ba3">IXpsOMImageResource</a> interface of the thumbnail resource that is associated with the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1be5c48-1e2b-4f94-98ec-b61bc255e63b">SetCoreProperties</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/705ec9c7-5aa9-4fc5-ad2c-441cb545d056">IXpsOMCoreProperties</a> interface of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce45f7cf-33ed-4e15-9f65-549ab2c8c8be">SetDiscardControlPartName</a>
</td>
<td align="left" width="63%">
Sets the name of the discard control part in the XPS package.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc159b7e-7cce-4f3b-ad0d-ce7b625b61d3">SetDocumentSequence</a>
</td>
<td align="left" width="63%">

              Sets the <a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a> interface of the XPS package.
            

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d5d5332-f6e1-4fad-8b45-c518196c17d2">SetThumbnailResource</a>
</td>
<td align="left" width="63%">
Sets the thumbnail image of the XPS document.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89accde7-989e-4a87-b96e-e47cc6c6954a">WriteToFile</a>
</td>
<td align="left" width="63%">
Writes the XPS package to a specified file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b729ac6-3f0e-4f24-b3f6-4b6d26844df1">WriteToStream</a>
</td>
<td align="left" width="63%">
Writes the XPS package to a specified stream.

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
IXpsOMPackage    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
      __uuidof(XpsOMObjectFactory),
      NULL, 
      CLSCTX_INPROC_SERVER,
      __uuidof(IXpsOMObjectFactory),
      reinterpret_cast&lt;LPVOID*&gt;(&amp;xpsFactory)
      );

if (SUCCEEDED(hr))
{
    hr = xpsFactory-&gt;CreatePackage (&amp;newInterface);
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
For information about using this interface in a program, see <a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a>



<a href="https://msdn.microsoft.com/c9319997-6c8f-4e2c-9401-ad269e3db8c8">IXpsOMObjectFactory::CreatePackage</a>



<a href="https://msdn.microsoft.com/2498792b-a33c-47cd-8d88-8e89b99c432d">IXpsOMObjectFactory::CreatePackageFromFile</a>



<a href="https://msdn.microsoft.com/4a4bb128-9480-4e50-8848-a2e1e715f4e3">IXpsOMObjectFactory::CreatePackageFromStream</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


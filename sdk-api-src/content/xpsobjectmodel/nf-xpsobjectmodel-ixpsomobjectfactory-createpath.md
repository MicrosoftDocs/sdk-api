---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePath
title: IXpsOMObjectFactory::CreatePath
author: windows-sdk-content
description: Creates an IXpsOMPath interface that specifies a graphical path element on a page.
old-location: xps\ixpsomobjectfactory_createpath.htm
tech.root: printdocs
ms.assetid: aa5dcddd-9ca7-4b8f-9f4f-aa0f851e8697
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreatePath, CreatePath method [XPS Documents and Packaging], CreatePath method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePath method, IXpsOMObjectFactory.CreatePath, IXpsOMObjectFactory::CreatePath, xps.ixpsomobjectfactory_createpath, xpsobjectmodel/IXpsOMObjectFactory::CreatePath
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
 - IXpsOMObjectFactory.CreatePath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMObjectFactory::CreatePath


## -description


Creates an <a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a> interface that specifies a graphical path element on a page.


## -parameters




### -param path [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a> interface.
          


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
<i>path</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The code example that follows illustrates how this method is used to create a new  interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
IXpsOMPath    *newInterface;

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
    hr = xpsFactory-&gt;CreatePath (&amp;newInterface);

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




<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


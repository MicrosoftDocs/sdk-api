---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePackage
title: IXpsOMObjectFactory::CreatePackage
author: windows-sdk-content
description: Creates an IXpsOMPackage interface that serves as the root node of an XPS object model document tree.
old-location: xps\ixpsomobjectfactory_createpackage.htm
old-project: printdocs
ms.assetid: c9319997-6c8f-4e2c-9401-ad269e3db8c8
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CreatePackage, CreatePackage method [XPS Documents and Packaging], CreatePackage method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePackage method, IXpsOMObjectFactory.CreatePackage, IXpsOMObjectFactory::CreatePackage, xps.ixpsomobjectfactory_createpackage, xpsobjectmodel/IXpsOMObjectFactory::CreatePackage
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMObjectFactory.CreatePackage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory::CreatePackage


## -description


Creates an <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface that serves as the root node of an XPS object model document tree.


## -parameters




### -param package [out, retval]

A pointer to the new <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface.
          


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
<i>package</i>  is <b>NULL</b>.

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
For information about using <a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a> interface in a program, see <a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a>.




## -see-also




<a href="https://msdn.microsoft.com/5b6f12ba-9a41-4252-96c4-391bb8d75cd4">Create a Blank XPS OM</a>



<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


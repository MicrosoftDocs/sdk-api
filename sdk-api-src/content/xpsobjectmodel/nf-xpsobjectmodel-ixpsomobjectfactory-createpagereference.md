---
UID: NF:xpsobjectmodel.IXpsOMObjectFactory.CreatePageReference
title: IXpsOMObjectFactory::CreatePageReference
author: windows-sdk-content
description: Creates an IXpsOMPageReference interface that enables the virtualization of pages.
old-location: xps\ixpsomobjectfactory_createpagereference.htm
old-project: printdocs
ms.assetid: 037a7926-def4-4be3-b7c5-3c4c588e75ae
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CreatePageReference, CreatePageReference method [XPS Documents and Packaging], CreatePageReference method [XPS Documents and Packaging],IXpsOMObjectFactory interface, IXpsOMObjectFactory interface [XPS Documents and Packaging],CreatePageReference method, IXpsOMObjectFactory.CreatePageReference, IXpsOMObjectFactory::CreatePageReference, xps.ixpsomobjectfactory_createpagereference, xpsobjectmodel/IXpsOMObjectFactory::CreatePageReference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
 - IXpsOMObjectFactory.CreatePageReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMObjectFactory::CreatePageReference


## -description


Creates an <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface that enables the virtualization of pages.


## -parameters




### -param advisoryPageDimensions [in]

The <a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a> structure that sets the advisory page dimensions (page width and  page height).
          

Size is described in XPS units. There are 96 XPS units per inch. For example, the dimensions of an 8.5" by 11.0" page are 816 by 1,056 XPS units.


### -param pageReference [out, retval]

A pointer to the new  <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interface.


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
<i>advisoryPageDimensions</i>  or   <i>pageReference</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_PAGE_SIZE</b></dt>
</dl>
</td>
<td width="60%">
<i>advisoryPageDimensions</i> contains an invalid page size or invalid page size values.

</td>
</tr>
</table>
 




## -remarks



 The use of a page reference makes it possible to delay the loading  of the full object model of a page until the loading is requested explicitly. If the page has not been altered, it  can be unloaded on request.

The code example that follows illustrates how this method is used to create a new  interface.


```cpp

IXpsOMPageReference    *newInterface;
// The following value is defined outside of 
// this example.
XPS_SIZE        advisoryPageDimensions;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsOMObjectFactory),
    NULL,
    CLSCTX_INPROC_SERVER,
    _uuidof(IXpsOMObjectFactory),
    reinterpret_cast<LPVOID*>(&xpsFactory)
    );

if (SUCCEEDED(hr))
{
    hr = xpsFactory->CreatePageReference (
        &advisoryPageDimensions,
        &newInterface);

    if (SUCCEEDED(hr))
    {
        // use newInterface

        newInterface->Release();
    }
    xpsFactory->Release();
}
else
{
    // evaluate HRESULT error returned in hr
}

```





## -see-also




<a href="https://msdn.microsoft.com/2444703e-4b89-4ef0-9ed7-aa937bc62e8c">IXpsOMObjectFactory</a>



<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/2f6eb553-892b-455b-97a5-280f257b5702">XPS_SIZE</a>
 

 


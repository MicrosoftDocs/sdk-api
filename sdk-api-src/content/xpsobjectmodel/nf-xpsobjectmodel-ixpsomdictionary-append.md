---
UID: NF:xpsobjectmodel.IXpsOMDictionary.Append
title: IXpsOMDictionary::Append (xpsobjectmodel.h)
author: windows-sdk-content
description: Appends an IXpsOMShareable interface along with its key to the end of the dictionary.
old-location: xps\ixpsomdictionary_append.htm
tech.root: printdocs
ms.assetid: 69df1cdc-a965-4ea8-b1af-75176caa39ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Append, Append method [XPS Documents and Packaging], Append method [XPS Documents and Packaging],IXpsOMDictionary interface, IXpsOMDictionary interface [XPS Documents and Packaging],Append method, IXpsOMDictionary.Append, IXpsOMDictionary::Append, xps.ixpsomdictionary_append, xpsobjectmodel/IXpsOMDictionary::Append
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
 - IXpsOMDictionary.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMDictionary::Append


## -description


Appends an <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface along with its <i>key</i> to the end of the dictionary.


## -parameters




### -param key [in]

The key to be used for this entry.

The string referenced by <i>key</i> must be unique in the dictionary.


### -param entry [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface that is to be appended  to the dictionary.

A dictionary cannot contain duplicate interface pointers. This parameter must contain an interface pointer that is not already in the dictionary.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>entry</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



The interface pointers stored in a dictionary will usually point to interfaces, such as <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>                 and <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>, that are derived from the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomshareable-gettype">IXpsOMShareable::GetType</a> method.

The figure that follows illustrates how the dictionary is changed by the <b>Append</b> method.

<img alt="A figure that shows how Append adds an entry to the dictionary" src="../images/dictionary_append.png"/>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush">IXpsOMBrush</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomshareable">IXpsOMShareable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 


---
UID: NF:xpsobjectmodel.IXpsOMDictionary.Append
title: IXpsOMDictionary::Append
author: windows-sdk-content
description: Appends an IXpsOMShareable interface along with its key to the end of the dictionary.
old-location: xps\ixpsomdictionary_append.htm
tech.root: printdocs
ms.assetid: 69df1cdc-a965-4ea8-b1af-75176caa39ee
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: Append, Append method [XPS Documents and Packaging], Append method [XPS Documents and Packaging],IXpsOMDictionary interface, IXpsOMDictionary interface [XPS Documents and Packaging],Append method, IXpsOMDictionary.Append, IXpsOMDictionary::Append, xps.ixpsomdictionary_append, xpsobjectmodel/IXpsOMDictionary::Append
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
 - IXpsOMDictionary.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDictionary::Append


## -description


Appends an <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface along with its <i>key</i> to the end of the dictionary.


## -parameters




### -param key [in]

The key to be used for this entry.

The string referenced by <i>key</i> must be unique in the dictionary.


### -param entry [in]

A pointer to the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface that is to be appended  to the dictionary.

A dictionary cannot contain duplicate interface pointers. This parameter must contain an interface pointer that is not already in the dictionary.


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
<i>entry</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



The interface pointers stored in a dictionary will usually point to interfaces, such as <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>                 and <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>, that are derived from the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="https://msdn.microsoft.com/1d30e11e-1306-4721-b5fc-0419715ba2c8">IXpsOMShareable::GetType</a> method.

The figure that follows illustrates how the dictionary is changed by the <b>Append</b> method.

<img alt="A figure that shows how Append adds an entry to the dictionary" src="../images/dictionary_append.png"/>



## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a>



<a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


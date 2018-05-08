---
UID: NF:xpsobjectmodel.IXpsOMDictionary.InsertAt
title: IXpsOMDictionary::InsertAt
author: windows-driver-content
description: Inserts an IXpsOMShareable interface at a specified location in the dictionary and sets the key to identify the interface.
old-location: xps\ixpsomdictionary_insertat.htm
old-project: printdocs
ms.assetid: a47b7130-a3c3-44d2-a987-e78b7feb52d6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMDictionary interface [XPS Documents and Packaging],InsertAt method, IXpsOMDictionary.InsertAt, IXpsOMDictionary::InsertAt, InsertAt, InsertAt method [XPS Documents and Packaging], InsertAt method [XPS Documents and Packaging],IXpsOMDictionary interface, xps.ixpsomdictionary_insertat, xpsobjectmodel/IXpsOMDictionary::InsertAt
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IXpsOMDictionary.InsertAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDictionary::InsertAt


## -description


Inserts an <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface at a specified location in the dictionary and sets the key to identify the interface.


## -parameters




### -param index [in]

The zero-based index in the dictionary where the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface is to be inserted.


### -param key [in]

The key to be used to identify the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface in the dictionary.

The string referenced by <i>key</i> must be unique in the dictionary.


### -param entry [in]

The <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface pointer to be inserted at the location specified by <i>index</i>.

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



The interface pointers stored in the dictionary will usually be pointers to interfaces, such as <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>                 and <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>, that are derived from the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface. To determine the interface type, call the <a href="https://msdn.microsoft.com/1d30e11e-1306-4721-b5fc-0419715ba2c8">IXpsOMShareable::GetType</a> method.

At the location specified by <i>index</i>, this method inserts the <a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a> interface pointer and  sets the key;  the interface pointer and key are passed in <i>value</i> and <i>key</i>, respectively.  Before <i>value</i> and <i>key</i> are inserted, the interface pointer and the key at this and all subsequent locations  are moved up by one index.

The figure that follows illustrates how the dictionary is changed by the <b>InsertAt</b> method.

<img alt="A figure that shows how InsertAt adds an entry to the dictionary" src="../images/dictionary_insertat.png"/>



## -see-also




<a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a>



<a href="https://msdn.microsoft.com/2071292f-b898-4ec8-99f7-294c8d820965">IXpsOMShareable</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


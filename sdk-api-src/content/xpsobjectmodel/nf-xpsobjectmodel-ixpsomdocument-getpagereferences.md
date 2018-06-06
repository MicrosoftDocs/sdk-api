---
UID: NF:xpsobjectmodel.IXpsOMDocument.GetPageReferences
title: IXpsOMDocument::GetPageReferences
author: windows-sdk-content
description: Gets the IXpsOMPageReferenceCollection interface of the document, which allows virtualized access to its pages.
old-location: xps\ixpsomdocument_getpagereferences.htm
old-project: printdocs
ms.assetid: 65e8b20b-6a6b-4d24-86a1-b9d1833caa3c
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetPageReferences, GetPageReferences method [XPS Documents and Packaging], GetPageReferences method [XPS Documents and Packaging],IXpsOMDocument interface, IXpsOMDocument interface [XPS Documents and Packaging],GetPageReferences method, IXpsOMDocument.GetPageReferences, IXpsOMDocument::GetPageReferences, xps.ixpsomdocument_getpagereferences, xpsobjectmodel/IXpsOMDocument::GetPageReferences
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
 - IXpsOMDocument.GetPageReferences
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocument::GetPageReferences


## -description


Gets the <a href="https://msdn.microsoft.com/4b51bc29-c653-41fa-bbd3-9ff529f84e4e">IXpsOMPageReferenceCollection</a> interface of the document, which allows virtualized access to its pages.


## -parameters




### -param pageReferences [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/4b51bc29-c653-41fa-bbd3-9ff529f84e4e">IXpsOMPageReferenceCollection</a> interface that contains a collection of page references for each page of the document. If there are no page references, the <b>IXpsOMPageReferenceCollection</b> returned in <i>pageReferences</i> will be empty and will have no elements.


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
<i>pageReferences</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



To get the pages of a document, first get the list of <a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a> interfaces by calling <b>GetPageReferences</b>. Then, for each  <b>IXpsOMPageReference</b> interface, load a page by calling <a href="https://msdn.microsoft.com/0004217f-f379-4175-bbce-eea93d96f37f">GetPage</a>.

If the document does not have any pages, the page reference collection returned in <i>pageReferences</i> will be empty. To get  the number of page references in the collection, call its <a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a> method.

For an example of how this method can be used in a program, see <a href="https://msdn.microsoft.com/90b726aa-29da-4cfb-9c69-f471c2acb678">Navigate the XPS OM</a>.




## -see-also




<a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a>



<a href="https://msdn.microsoft.com/cdebab24-f918-4235-b4d5-5ee1007ade87">IXpsOMPageReference</a>



<a href="https://msdn.microsoft.com/4b51bc29-c653-41fa-bbd3-9ff529f84e4e">IXpsOMPageReferenceCollection</a>



<a href="https://msdn.microsoft.com/90b726aa-29da-4cfb-9c69-f471c2acb678">Navigate the XPS OM</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


---
UID: NF:xpsobjectmodel.IXpsOMDocument.SetDocumentStructureResource
title: IXpsOMDocument::SetDocumentStructureResource
author: windows-sdk-content
description: Sets the IXpsOMDocumentStructureResource interface for the document.
old-location: xps\ixpsomdocument_setdocumentstructureresource.htm
tech.root: printdocs
ms.assetid: 86d62b73-b7a7-4470-9e55-f4eab50531d0
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMDocument interface [XPS Documents and Packaging],SetDocumentStructureResource method, IXpsOMDocument.SetDocumentStructureResource, IXpsOMDocument::SetDocumentStructureResource, SetDocumentStructureResource, SetDocumentStructureResource method [XPS Documents and Packaging], SetDocumentStructureResource method [XPS Documents and Packaging],IXpsOMDocument interface, xps.ixpsomdocument_setdocumentstructureresource, xpsobjectmodel/IXpsOMDocument::SetDocumentStructureResource
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
 - IXpsOMDocument.SetDocumentStructureResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMDocument::SetDocumentStructureResource


## -description


Sets the <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface for the document.
        


## -parameters




### -param documentStructureResource [in]

A pointer to the <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface to be assigned to the document.
          A <b>NULL</b> pointer releases any previously assigned resource.


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
<i>documentStructureResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



If the document contains an <a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a> interface when this method is called, that interface is released before the new <b>IXpsOMDocumentStructureResource</b> interface, which is passed in <i>documentStructureResource</i>, is set.




## -see-also




<a href="https://msdn.microsoft.com/22d3c0a1-3ad5-4f48-9e1e-eaf3bd95b39f">IXpsOMDocument</a>



<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


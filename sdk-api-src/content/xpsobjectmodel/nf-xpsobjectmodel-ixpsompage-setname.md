---
UID: NF:xpsobjectmodel.IXpsOMPage.SetName
title: IXpsOMPage::SetName
author: windows-sdk-content
description: Sets the Name property of this page.
old-location: xps\ixpsompage_setname.htm
old-project: printdocs
ms.assetid: 675e4fd2-e8b9-400f-9042-df5b0bb0b89a
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IXpsOMPage interface [XPS Documents and Packaging],SetName method, IXpsOMPage.SetName, IXpsOMPage::SetName, SetName, SetName method [XPS Documents and Packaging], SetName method [XPS Documents and Packaging],IXpsOMPage interface, xps.ixpsompage_setname, xpsobjectmodel/IXpsOMPage::SetName
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
 - IXpsOMPage.SetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPage::SetName


## -description


Sets the <b>Name</b> property of this page.


## -parameters




### -param name [in]

A pointer to the name string to be set as the page's <b>Name</b> property. A <b>NULL</b> pointer clears any previously assigned name.


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
<dt><b>XPS_E_INVALID_NAME</b></dt>
</dl>
</td>
<td width="60%">
The name string contains a character that is not valid.

</td>
</tr>
</table>
 




## -remarks



The <b>Name</b> property identifies the current page as a named, addressable point in a document, allowing the page to be referenced by a hyperlink.




## -see-also




<a href="https://msdn.microsoft.com/741deebd-9dce-4cd9-883e-4586c10a4609">IXpsOMPage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


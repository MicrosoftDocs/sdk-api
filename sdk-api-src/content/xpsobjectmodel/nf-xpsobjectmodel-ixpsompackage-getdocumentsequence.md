---
UID: NF:xpsobjectmodel.IXpsOMPackage.GetDocumentSequence
title: IXpsOMPackage::GetDocumentSequence
author: windows-sdk-content
description: Gets a pointer to the IXpsOMDocumentSequence interface that contains the document sequence of the XPS package.
old-location: xps\ixpsompackage_getdocumentsequence.htm
tech.root: printdocs
ms.assetid: 30789376-1ac8-41ae-9c4d-e3d2d0715016
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDocumentSequence, GetDocumentSequence method [XPS Documents and Packaging], GetDocumentSequence method [XPS Documents and Packaging],IXpsOMPackage interface, IXpsOMPackage interface [XPS Documents and Packaging],GetDocumentSequence method, IXpsOMPackage.GetDocumentSequence, IXpsOMPackage::GetDocumentSequence, xps.ixpsompackage_getdocumentsequence, xpsobjectmodel/IXpsOMPackage::GetDocumentSequence
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
 - IXpsOMPackage.GetDocumentSequence
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPackage::GetDocumentSequence


## -description


Gets a pointer to the  <a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a> interface that contains the document sequence of the XPS package.


## -parameters




### -param documentSequence [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a> interface that contains the document sequence of the  XPS package. If an <b>IXpsOMDocumentSequence</b> interface has not been set, a <b>NULL</b> pointer is returned.


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
<i>documentSequence</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a>



<a href="https://msdn.microsoft.com/7b0a36d6-1af1-4c2c-af14-d6139e9115c3">IXpsOMPackage</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


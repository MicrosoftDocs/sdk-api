---
UID: NF:xpsobjectmodel.IXpsOMDocumentSequence.GetDocuments
title: IXpsOMDocumentSequence::GetDocuments
author: windows-sdk-content
description: Gets a pointer to the IXpsOMDocumentCollection interface, which contains the documents specified in the document sequence.
old-location: xps\ixpsomdocumentsequence_getdocuments.htm
old-project: printdocs
ms.assetid: d924e610-1142-4623-b64b-219558fb07d6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDocuments, GetDocuments method [XPS Documents and Packaging], GetDocuments method [XPS Documents and Packaging],IXpsOMDocumentSequence interface, IXpsOMDocumentSequence interface [XPS Documents and Packaging],GetDocuments method, IXpsOMDocumentSequence.GetDocuments, IXpsOMDocumentSequence::GetDocuments, xps.ixpsomdocumentsequence_getdocuments, xpsobjectmodel/IXpsOMDocumentSequence::GetDocuments
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMDocumentSequence.GetDocuments
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocumentSequence::GetDocuments


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/4f3acae9-10a0-47ff-9170-a40abe230580">IXpsOMDocumentCollection</a> interface, which contains the documents specified in the document sequence.


## -parameters




### -param documents [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/4f3acae9-10a0-47ff-9170-a40abe230580">IXpsOMDocumentCollection</a> interface, which contains the documents specified in the document sequence. If the sequence does not have any documents, the <b>IXpsOMDocumentCollection</b> interface will be empty.


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
<i>documents</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If the document sequence does not have any documents, the document collection that is returned in <i>documents</i> will be empty. To get  the number of documents in the collection, call the collection's <a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a> method.




## -see-also




<a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


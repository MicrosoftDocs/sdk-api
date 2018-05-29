---
UID: NF:xpsobjectmodel.IXpsOMDocumentSequence.GetPrintTicketResource
title: IXpsOMDocumentSequence::GetPrintTicketResource
author: windows-sdk-content
description: Gets the IXpsOMPrintTicketResource interface to the job-level print ticket that is assigned to the document sequence.
old-location: xps\ixpsomdocumentsequence_getprintticketresource.htm
old-project: printdocs
ms.assetid: 0d53d537-8db1-4e39-98e6-8987dbf5fc27
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetPrintTicketResource, GetPrintTicketResource method [XPS Documents and Packaging], GetPrintTicketResource method [XPS Documents and Packaging],IXpsOMDocumentSequence interface, IXpsOMDocumentSequence interface [XPS Documents and Packaging],GetPrintTicketResource method, IXpsOMDocumentSequence.GetPrintTicketResource, IXpsOMDocumentSequence::GetPrintTicketResource, xps.ixpsomdocumentsequence_getprintticketresource, xpsobjectmodel/IXpsOMDocumentSequence::GetPrintTicketResource
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
-	IXpsOMDocumentSequence.GetPrintTicketResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocumentSequence::GetPrintTicketResource


## -description


Gets the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface to the job-level print ticket that is  assigned to the document sequence.


## -parameters




### -param printTicketResource [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface of the job-level print ticket that is  assigned to the document sequence. If no <b>IXpsOMPrintTicketResource</b> interface has been assigned to the document sequence, a <b>NULL</b> pointer is returned.


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
<i>printTicketResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


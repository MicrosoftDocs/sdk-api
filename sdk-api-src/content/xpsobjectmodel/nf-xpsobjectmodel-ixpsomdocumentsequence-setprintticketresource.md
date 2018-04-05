---
UID: NF:xpsobjectmodel.IXpsOMDocumentSequence.SetPrintTicketResource
title: IXpsOMDocumentSequence::SetPrintTicketResource method
author: windows-driver-content
description: Sets the job-level print ticket resource for the document sequence.
old-location: xps\ixpsomdocumentsequence_setprintticketresource.htm
old-project: printdocs
ms.assetid: bfc5889d-ab1d-4dbe-af11-625ee5e8c95f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMDocumentSequence, IXpsOMDocumentSequence interface [XPS Documents and Packaging], SetPrintTicketResource method, IXpsOMDocumentSequence::SetPrintTicketResource, SetPrintTicketResource method [XPS Documents and Packaging], SetPrintTicketResource method [XPS Documents and Packaging], IXpsOMDocumentSequence interface, SetPrintTicketResource,IXpsOMDocumentSequence.SetPrintTicketResource, xps.ixpsomdocumentsequence_setprintticketresource, xpsobjectmodel/IXpsOMDocumentSequence::SetPrintTicketResource
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
-	IXpsOMDocumentSequence.SetPrintTicketResource
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocumentSequence::SetPrintTicketResource method


## -description


Sets the job-level print ticket resource for the document sequence.


## -parameters




### -param printTicketResource [in]

A pointer to the  <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface of the job-level print ticket that will be set for the document sequence.
          If the document sequence has a print ticket resource, a <b>NULL</b> pointer will release it.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



If the document contains an <a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a> interface when this method is called, that interface is released before the new <b>IXpsOMPrintTicketResource</b> interface, which is passed in <i>printTicketResource</i>, is set.




## -see-also




<a href="https://msdn.microsoft.com/472095a4-ecd8-406a-97c2-1a34b4e5184a">IXpsOMDocumentSequence</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


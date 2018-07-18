---
UID: NF:xpsobjectmodel.IXpsOMDocumentStructureResource.SetContent
title: IXpsOMDocumentStructureResource::SetContent
author: windows-sdk-content
description: Sets the read-only stream to be associated with this resource.
old-location: xps\ixpsomdocumentstructureresource_setcontent.htm
old-project: printdocs
ms.assetid: 0b58e0ca-03e7-43ea-aab2-5ac6cdb15807
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMDocumentStructureResource interface [XPS Documents and Packaging],SetContent method, IXpsOMDocumentStructureResource.SetContent, IXpsOMDocumentStructureResource::SetContent, SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging],IXpsOMDocumentStructureResource interface, xps.ixpsomdocumentstructureresource_setcontent, xpsobjectmodel/IXpsOMDocumentStructureResource::SetContent
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
 - IXpsOMDocumentStructureResource.SetContent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMDocumentStructureResource::SetContent


## -description


Sets the read-only stream to be associated with this resource.


## -parameters




### -param sourceStream [in]

The read-only stream to be associated with this resource.


### -param partName [in]

The part name to be assigned to this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The calling method  should treat this stream as a single-threaded apartment (STA) model object and not re-enter any of the stream interface's methods.

For more information about the content of DocumentStructure part, see the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>.

Because <a href="https://msdn.microsoft.com/77c08ced-bc0d-4ebf-a257-d4298c7a352d">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/a0cc8748-08b2-4471-9961-603786e983a4">IXpsOMDocumentStructureResource</a>



<a href="https://msdn.microsoft.com/b4cd8f69-3559-46a0-95ec-6fcaab21959c">Packaging Errors</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 


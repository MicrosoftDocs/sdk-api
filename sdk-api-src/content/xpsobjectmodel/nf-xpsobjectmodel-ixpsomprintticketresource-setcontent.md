---
UID: NF:xpsobjectmodel.IXpsOMPrintTicketResource.SetContent
title: IXpsOMPrintTicketResource::SetContent
author: windows-sdk-content
description: Sets the read-only stream to be associated with this resource.
old-location: xps\ixpsomprintticketresource_setcontent.htm
tech.root: printdocs
ms.assetid: 77e4af00-b2ed-4c88-80f1-fb3106ad1e75
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXpsOMPrintTicketResource interface [XPS Documents and Packaging],SetContent method, IXpsOMPrintTicketResource.SetContent, IXpsOMPrintTicketResource::SetContent, SetContent, SetContent method [XPS Documents and Packaging], SetContent method [XPS Documents and Packaging],IXpsOMPrintTicketResource interface, xps.ixpsomprintticketresource_setcontent, xpsobjectmodel/IXpsOMPrintTicketResource::SetContent
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
 - IXpsOMPrintTicketResource.SetContent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMPrintTicketResource.SetContent
: 
---

# IXpsOMPrintTicketResource::SetContent


## -description


Sets the read-only stream to be  associated with this resource.


## -parameters




### -param sourceStream [in]

The read-only stream to be associated with this resource.


### -param partName [in]

The part name to be assigned to this resource.


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The calling method  should treat this stream as a single-threaded apartment (STA) model object and not re-enter any of the stream interface's methods.

Because <a href="https://msdn.microsoft.com/0783cdda-84c6-4441-accf-10fc2610199b">GetStream</a> gets a clone of  the stream that is set by this method, the provided stream should have an efficient cloning method. A stream with an inefficient cloning method will reduce the performance of <b>GetStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/81123212-7a32-4833-b81f-8454a544327d">IOpcPartUri</a>



<a href="https://msdn.microsoft.com/2f37dbd2-3078-4aa8-97e7-556a0ff2dd74">IXpsOMPrintTicketResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


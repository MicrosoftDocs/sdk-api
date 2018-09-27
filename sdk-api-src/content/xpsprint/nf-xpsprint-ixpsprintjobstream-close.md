---
UID: NF:xpsprint.IXpsPrintJobStream.Close
title: IXpsPrintJobStream::Close
author: windows-sdk-content
description: Closes the stream and indicates to the print job that the entire document has been written to the print queue by the application.
old-location: gdi\ixpsprintjobstream_close.htm
tech.root: printdocs
ms.assetid: 259d0224-4e6e-43c8-905d-3529c781986a
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Close, Close method [Windows GDI], Close method [Windows GDI],IXpsPrintJobStream interface, IXpsPrintJobStream interface [Windows GDI],Close method, IXpsPrintJobStream.Close, IXpsPrintJobStream::Close, gdi.ixpsprintjobstream_close, xpsprint/IXpsPrintJobStream::Close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsprint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - XpsPrint.h
api_name:
 - IXpsPrintJobStream.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsPrintJobStream::Close


## -description


<p class="CCE_Message">[IXpsPrintJobStream::Close is not supported and may be altered or unavailable in the future. ]

Closes the stream and indicates to the print job that the entire document has been written to the print queue by the application.


## -parameters






## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



After <b>Close</b> has been called, all subsequent attempts to write data to the stream will fail.




## -see-also




<a href="https://msdn.microsoft.com/14ae2c97-8596-46db-a55c-ef706d2cd00b">Documents</a>



<a href="https://msdn.microsoft.com/a7855015-32db-48ff-8f8d-3d84d2843fde">IXpsPrintJobStream</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 


---
UID: NF:strmif.IAsyncReader.EndFlush
title: IAsyncReader::EndFlush
author: windows-sdk-content
description: The EndFlush method ends a flush operation.
old-location: dshow\iasyncreader_endflush.htm
tech.root: DirectShow
ms.assetid: 38a7fd8a-c027-49fd-8f52-49ddf072fe02
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: EndFlush, EndFlush method [DirectShow], EndFlush method [DirectShow],IAsyncReader interface, IAsyncReader interface [DirectShow],EndFlush method, IAsyncReader.EndFlush, IAsyncReader::EndFlush, IAsyncReaderEndFlush, dshow.iasyncreader_endflush, strmif/IAsyncReader::EndFlush
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAsyncReader.EndFlush
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAsyncReader::EndFlush


## -description



The <code>EndFlush</code> method ends a flush operation.




## -parameters






## -returns



Returns S_OK if successful, or S_FALSE otherwise.




## -remarks



While the pin is flushing, the <a href="https://msdn.microsoft.com/d0eab370-bb17-48fa-9926-6a6eeaba5603">IAsyncReader::Request</a> method fails and the <a href="https://msdn.microsoft.com/fc54f917-3b86-4c0b-b356-217bc9793504">IAsyncReader::WaitForNext</a> method returns immediately. Call the <code>EndFlush</code> method at the end of a flush operation, to reenable the <b>Request</b> method.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/54a18567-e9d4-4b12-b486-cdd70d719184">IAsyncReader Interface</a>
 

 


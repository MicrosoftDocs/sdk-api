---
UID: NF:wmsdkidl.IWMWriterFileSink3.CompleteOperations
title: IWMWriterFileSink3::CompleteOperations
author: windows-sdk-content
description: The CompleteOperations method stops the writer sink after completing all operations in progress. This method is used with unbuffered I/O.
old-location: wmformat\iwmwriterfilesink3_completeoperations.htm
tech.root: wmformat
ms.assetid: 6eb4f09f-627e-4409-9f08-8f655aa7d0ec
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CompleteOperations, CompleteOperations method [windows Media Format], CompleteOperations method [windows Media Format],IWMWriterFileSink3 interface, IWMWriterFileSink3 interface [windows Media Format],CompleteOperations method, IWMWriterFileSink3.CompleteOperations, IWMWriterFileSink3::CompleteOperations, IWMWriterFileSink3CompleteOperations, wmformat.iwmwriterfilesink3_completeoperations, wmsdkidl/IWMWriterFileSink3::CompleteOperations
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMWriterFileSink3.CompleteOperations
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMWriterFileSink3::CompleteOperations


## -description



The <b>CompleteOperations</b> method stops the writer sink after completing all operations in progress. This method is used with unbuffered I/O.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method is called when writes are performed as a result of calls to <a href="https://msdn.microsoft.com/97b1dbd0-a555-40d3-b2f0-3a363a6ce168">IWMWriterSink::OnHeader</a>, <a href="https://msdn.microsoft.com/32e52cdb-e7cb-4caf-a202-0d2ff746017c">IWMWriterSink::OnDataUnit</a>, and <a href="https://msdn.microsoft.com/1dbcb27b-7588-4475-99fe-3e547d1659d3">IWMWriterFileSink3::OnDataUnitEx</a>. Applications do not call this method.




## -see-also




<a href="https://msdn.microsoft.com/67f418c8-184d-46f0-8939-69194c7e7a50">IWMWriterFileSink3 Interface</a>



<a href="https://msdn.microsoft.com/51a9c21b-d301-41e4-a9bc-321a5b2decca">IWMWriterFileSink3::SetUnbufferedIO</a>
 

 


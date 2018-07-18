---
UID: NF:wmsdkidl.IWMWriterFileSink2.Stop
title: IWMWriterFileSink2::Stop
author: windows-sdk-content
description: The Stop method stops recording at the specified time.
old-location: wmformat\iwmwriterfilesink2_stop.htm
old-project: wmformat
ms.assetid: 47377c77-f534-4bb0-be57-49bdb109c309
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMWriterFileSink2 interface [windows Media Format],Stop method, IWMWriterFileSink2.Stop, IWMWriterFileSink2::Stop, IWMWriterFileSink2Stop, Stop, Stop method [windows Media Format], Stop method [windows Media Format],IWMWriterFileSink2 interface, wmformat.iwmwriterfilesink2_stop, wmsdkidl/IWMWriterFileSink2::Stop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMWriterFileSink2.Stop
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterFileSink2::Stop


## -description



The <b>Stop</b> method stops recording at the specified time.




## -parameters




### -param cnsStopTime [in]

Stop time in 100-nanosecond units.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Because of interleaving of streams with slightly different time stamps at any particular point in the file, the actual stop time might not be exactly as specified in <i>cnsStopTime</i>. To increase the precision, call <a href="https://msdn.microsoft.com/c103d205-a568-4206-a66e-5473e16cfa3f">IWMWriterFileSink3::SetControlStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/229ae2a5-103a-4a33-b7ca-c9b2854c6741">IWMWriterFileSink2 Interface</a>



<a href="https://msdn.microsoft.com/8d1bce07-a165-45cf-95cb-03b57f0cae03">IWMWriterFileSink2::Close</a>



<a href="https://msdn.microsoft.com/b4bfddbb-9156-42bf-b8d5-424fff9f4b64">IWMWriterFileSink2::Start</a>
 

 


---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetAllocateForStream
title: IWMReaderAdvanced::SetAllocateForStream
author: windows-sdk-content
description: The SetAllocateForStream method specifies whether the reader uses IWMReaderCallbackAdvanced::AllocateForStream to allocate buffers for stream samples.
old-location: wmformat\iwmreaderadvanced_setallocateforstream.htm
old-project: wmformat
ms.assetid: 58c396a9-5d1e-4a13-a877-5289649a6375
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetAllocateForStream method, IWMReaderAdvanced.SetAllocateForStream, IWMReaderAdvanced::SetAllocateForStream, IWMReaderAdvancedSetAllocateForStream, SetAllocateForStream, SetAllocateForStream method [windows Media Format], SetAllocateForStream method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setallocateforstream, wmsdkidl/IWMReaderAdvanced::SetAllocateForStream
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
 - IWMReaderAdvanced.SetAllocateForStream
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::SetAllocateForStream


## -description



The <b>SetAllocateForStream</b> method specifies whether the reader uses <a href="https://msdn.microsoft.com/82d31f4b-d8a8-4538-be5e-dd9149e3f420">IWMReaderCallbackAdvanced::AllocateForStream</a> to allocate buffers for stream samples.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers are in the range of 1 through 63.


### -param fAllocate [in]

Boolean value that is True if the reader uses <b>IWMReaderCallbackAdvanced</b> to allocate streams.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



If the application's callback implements the <a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx</a> interface interface, the <a href="https://msdn.microsoft.com/bb12f0e1-dc9c-447e-a28d-30c45eb95d09">AllocateForStreamEx</a> method is called instead of <b>AllocateForStream</b>.




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/816f13b1-9856-482d-b5b1-4aaf5c61c230">IWMReaderAdvanced::GetAllocateForStream</a>



<a href="https://msdn.microsoft.com/bb12f0e1-dc9c-447e-a28d-30c45eb95d09">IWMReaderAllocatorEx::AllocateForStreamEx</a>
 

 


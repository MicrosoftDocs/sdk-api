---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetAllocateForOutput
title: IWMReaderAdvanced::SetAllocateForOutput
author: windows-sdk-content
description: The SetAllocateForOutput method specifies whether the reader allocates its own buffers for output samples or gets buffers from your application.
old-location: wmformat\iwmreaderadvanced_setallocateforoutput.htm
old-project: wmformat
ms.assetid: fba76c75-6179-4e10-9a3c-8e604e392cca
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetAllocateForOutput method, IWMReaderAdvanced.SetAllocateForOutput, IWMReaderAdvanced::SetAllocateForOutput, IWMReaderAdvancedSetAllocateForOutput, SetAllocateForOutput, SetAllocateForOutput method [windows Media Format], SetAllocateForOutput method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setallocateforoutput, wmsdkidl/IWMReaderAdvanced::SetAllocateForOutput
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
 - IWMReaderAdvanced.SetAllocateForOutput
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::SetAllocateForOutput


## -description



The <b>SetAllocateForOutput</b> method specifies whether the reader allocates its own buffers for output samples or gets buffers from your application.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param fAllocate [in]

Boolean value that is True if the reader gets buffers from your application.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



You can allocate your own buffers for file reading to reduce the overhead required by the reader object to allocate a new buffer for every sample. The reader object will make calls to the <b>IWMReaderCallbackAdvanced::AllocateForOutput</b> method.

If the application's callback implements the <a href="https://msdn.microsoft.com/be727c7b-b252-44db-825b-5c683e551fd2">IWMReaderAllocatorEx</a> interface, the <a href="https://msdn.microsoft.com/e2e4881b-2186-47c9-b74e-3a59a9fac7c9">AllocateForOutputEx</a> method is called instead of <b>AllocateForOutput</b>.




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/b0da74ff-37d9-4bb3-85f2-f8e1585c2d7f">IWMReaderAdvanced::GetAllocateForOutput</a>
 

 


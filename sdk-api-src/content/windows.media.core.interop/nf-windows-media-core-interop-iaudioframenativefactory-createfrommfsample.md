---
UID: NF:windows.media.core.interop.IAudioFrameNativeFactory.CreateFromMFSample
title: IAudioFrameNativeFactory::core
author: windows-sdk-content
description: Creates an IAudioFrameNative from the provided IMFSample.
old-location: winrt\iaudioframenativefactory_createfrommfsample.htm
old-project: WinRT
ms.assetid: 331F6479-855E-459B-843F-B4FC4C88ED76
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CreateFromMFSample, CreateFromMFSample method [Windows Runtime], CreateFromMFSample method [Windows Runtime],IAudioFrameNativeFactory interface, IAudioFrameNativeFactory interface [Windows Runtime],CreateFromMFSample method, IAudioFrameNativeFactory.CreateFromMFSample, IAudioFrameNativeFactory.core, IAudioFrameNativeFactory::CreateFromMFSample, IAudioFrameNativeFactory::core, windows/IAudioFrameNativeFactory::CreateFromMFSample, winrt.iaudioframenativefactory_createfrommfsample
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: windows.media.core.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: PDF_RENDER_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.core.interop.h
api_name:
 - IAudioFrameNativeFactory.CreateFromMFSample
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IAudioFrameNativeFactory::core


## -description


Creates an <a href="https://msdn.microsoft.com/9C9DDDFD-8399-403F-8EB4-485D8531C94B">IAudioFrameNative</a> from the provided <a href="https://msdn.microsoft.com/b1c3758c-5133-41ee-b991-ae99d0296ccc">IMFSample</a>.


## -parameters




### -param data [in]

Type: <b>IMFSample*</b>

The source buffer containing an audio frame.


### -param forceReadOnly [in]

Type: <b>BOOL</b>

A value indicating whether the created software audio frame is read-only.


### -param riid [in]

Type: <b>REFIID</b>

The IID of the <a href="https://msdn.microsoft.com/9C9DDDFD-8399-403F-8EB4-485D8531C94B">IAudioFrameNative</a> interface.


### -param ppv [out]

Type: <b>LPVOID*</b>

When this method returns successfully, contains the requested interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns S_OK on successful completion.




## -see-also




<a href="https://msdn.microsoft.com/8416020D-8CBA-4E70-B77C-55057E6212BA">IAudioFrameNativeFactory</a>
 

 


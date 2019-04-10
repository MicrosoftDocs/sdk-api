---
UID: NF:wmsdkidl.IWMPlayerHook.PreDecode
title: IWMPlayerHook::PreDecode (wmsdkidl.h)
author: windows-sdk-content
description: The PreDecode method is called by the reader object before a sample from the output to which the IWMPlayerHook interface is assigned is passed to the video processor for decoding.
old-location: wmformat\iwmplayerhook_predecode.htm
tech.root: wmformat
ms.assetid: 88a78360-3e67-4425-8c65-3f746c6c807d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPlayerHook interface [windows Media Format],PreDecode method, IWMPlayerHook.PreDecode, IWMPlayerHook::PreDecode, IWMPlayerHookPreDecode, PreDecode, PreDecode method [windows Media Format], PreDecode method [windows Media Format],IWMPlayerHook interface, wmformat.iwmplayerhook_predecode, wmsdkidl/IWMPlayerHook::PreDecode
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK with update number 888656 installed, or later versions of the SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IWMPlayerHook.PreDecode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPlayerHook::PreDecode


## -description



The <b>PreDecode</b> method is called by the reader object before a sample from the output to which the <b>IWMPlayerHook</b> interface is assigned is passed to the video processor for decoding.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. You should return S_OK.




## -remarks



To assign an implementation of the <b>IWMPlayerHook</b> interface to an output in the reader object, call <a href="https://msdn.microsoft.com/en-us/library/Dd757461(v=VS.85).aspx">IWMReaderAdvanced5::SetPlayerHook</a>.




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757261(v=VS.85).aspx">IWMPlayerHook Interface</a>
 

 


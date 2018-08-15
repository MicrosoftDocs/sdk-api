---
UID: NF:wmsdkidl.IWMPlayerHook.PreDecode
title: IWMPlayerHook::PreDecode
author: windows-sdk-content
description: The PreDecode method is called by the reader object before a sample from the output to which the IWMPlayerHook interface is assigned is passed to the video processor for decoding.
old-location: wmformat\iwmplayerhook_predecode.htm
old-project: wmformat
ms.assetid: 88a78360-3e67-4425-8c65-3f746c6c807d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMPlayerHook interface [windows Media Format],PreDecode method, IWMPlayerHook.PreDecode, IWMPlayerHook::PreDecode, IWMPlayerHookPreDecode, PreDecode, PreDecode method [windows Media Format], PreDecode method [windows Media Format],IWMPlayerHook interface, wmformat.iwmplayerhook_predecode, wmsdkidl/IWMPlayerHook::PreDecode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
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
 - IWMPlayerHook.PreDecode
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPlayerHook::PreDecode


## -description



The <b>PreDecode</b> method is called by the reader object before a sample from the output to which the <b>IWMPlayerHook</b> interface is assigned is passed to the video processor for decoding.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. You should return S_OK.




## -remarks



To assign an implementation of the <b>IWMPlayerHook</b> interface to an output in the reader object, call <a href="https://msdn.microsoft.com/499c6c31-8cdf-4b99-964a-1fd51c14c5bd">IWMReaderAdvanced5::SetPlayerHook</a>.




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/5e58cb6a-3398-4b12-881e-76f936f6c7b3">IWMPlayerHook Interface</a>
 

 


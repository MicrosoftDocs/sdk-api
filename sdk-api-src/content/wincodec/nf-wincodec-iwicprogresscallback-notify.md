---
UID: NF:wincodec.IWICProgressCallback.Notify
title: IWICProgressCallback::Notify
author: windows-driver-content
description: Notify method is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use RegisterProgressNotification.
old-location: wic\_wic_codec_iwicprogresscallback_notify.htm
old-project: wic
ms.assetid: afbbfa87-716c-4957-9f90-d48d02d642e0
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWICProgressCallback interface [Windows Imaging Component],Notify method, IWICProgressCallback.Notify, IWICProgressCallback::Notify, Notify, Notify method [Windows Imaging Component], Notify method [Windows Imaging Component],IWICProgressCallback interface, _wic_codec_iwicprogresscallback_notify, wic._wic_codec_iwicprogresscallback_notify, wincodec/IWICProgressCallback::Notify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICTiffCompressionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Windowscodecs.dll
api_name:
-	IWICProgressCallback.Notify
product: Windows
targetos: Windows
req.lib: 
req.dll: Windowscodecs.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICProgressCallback::Notify


## -description


<b>Notify</b> method is documented only for compliance; its use is not recommended and may be altered or unavailable in the future. Instead, and use <a href="https://msdn.microsoft.com/ac47178a-f149-4313-8673-ece59e88cfb3">RegisterProgressNotification</a>. 



## -parameters




### -param uFrameNum [in]

Type: <b>ULONG</b>

The current frame number.


### -param operation [in]

Type: <b><a href="https://msdn.microsoft.com/407b982d-7232-42ce-9ff5-7029b7d922a4">WICProgressOperation</a></b>

The operation on which progress is being reported.


### -param dblProgress [in]

Type: <b>double</b>

The progress value ranging from is 0.0 to 1.0. 0.0 indicates the beginning of the operation. 1.0 indicates the end of the operation.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cd94e0a1-c275-458e-ae7f-85b703fc660e">IWICProgressCallback</a>
 

 


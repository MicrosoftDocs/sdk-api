---
UID: NF:wincodec.IWICBitmapCodecProgressNotification.RegisterProgressNotification
title: IWICBitmapCodecProgressNotification::RegisterProgressNotification
author: windows-sdk-content
description: Registers a progress notification callback function.
old-location: wic\_wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification.htm
old-project: wic
ms.assetid: ac47178a-f149-4313-8673-ece59e88cfb3
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IWICBitmapCodecProgressNotification interface [Windows Imaging Component],RegisterProgressNotification method, IWICBitmapCodecProgressNotification.RegisterProgressNotification, IWICBitmapCodecProgressNotification::RegisterProgressNotification, RegisterProgressNotification, RegisterProgressNotification method [Windows Imaging Component], RegisterProgressNotification method [Windows Imaging Component],IWICBitmapCodecProgressNotification interface, _wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification, wic._wic_codec_iwicbitmapcodecprogressnotification_registerprogressnotification, wincodec/IWICBitmapCodecProgressNotification::RegisterProgressNotification
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WICTiffCompressionOption
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.lib
 - Windowscodecs.dll
api_name:
 - IWICBitmapCodecProgressNotification.RegisterProgressNotification
product: Windows
targetos: Windows
req.lib: Windowscodecs.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWICBitmapCodecProgressNotification::RegisterProgressNotification


## -description


Registers a progress notification callback function.


## -parameters




### -param pfnProgressNotification [in]

Type: <b>PFNProgressNotification</b>

A function pointer to the application defined progress notification callback function. See <a href="https://msdn.microsoft.com/10dd9fbe-abff-4fc9-a3a5-7c01ecc10a7f">ProgressNotificationCallback</a> for the callback signature.


### -param pvData [in]

Type: <b>LPVOID</b>

A pointer to component data for the callback method.


### -param dwProgressFlags [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/407b982d-7232-42ce-9ff5-7029b7d922a4">WICProgressOperation</a> and <a href="https://msdn.microsoft.com/6d7ef6f1-2024-4de5-9c2e-8edc6359f79b">WICProgressNotification</a> flags to use for progress notification.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Applications can only register a single callback. Subsequent registration calls will replace the previously registered callback. To unregister a callback, pass in <b>NULL</b> or register a new callback function.


            Progress is reported in an increasing order between 0.0 and 1.0. 
            If <i>dwProgressFlags</i> includes <b>WICProgressNotificationBegin</b>, the callback is guaranteed to be called with progress 0.0.
            If <i>dwProgressFlags</i> includes <b>WICProgressNotificationEnd</b>, the callback is guaranteed to be called with progress 1.0.
         

<b>WICProgressNotificationFrequent</b> increases the frequency in which the callback is called.
            If an operation is expected to take more than 30 seconds, <b>WICProgressNotificationFrequent</b> should be added to <i>dwProgressFlags</i>.
         




## -see-also




<a href="https://msdn.microsoft.com/8cf3fbca-0953-4dd7-aa44-3e1924cfd8b0">IWICBitmapCodecProgressNotification</a>



<a href="https://msdn.microsoft.com/10dd9fbe-abff-4fc9-a3a5-7c01ecc10a7f">ProgressNotificationCallback</a>
 

 


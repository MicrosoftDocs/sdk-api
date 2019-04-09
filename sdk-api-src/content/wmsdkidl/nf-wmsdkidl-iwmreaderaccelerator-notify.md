---
UID: NF:wmsdkidl.IWMReaderAccelerator.Notify
title: IWMReaderAccelerator::Notify (wmsdkidl.h)
author: windows-sdk-content
description: The Notify method is called by the source filter to pass in the negotiated media type.
old-location: wmformat\iwmreaderaccelerator_notify.htm
tech.root: wmformat
ms.assetid: b5381f3a-e120-4db3-8463-5286e4318b13
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMReaderAccelerator interface [windows Media Format],Notify method, IWMReaderAccelerator.Notify, IWMReaderAccelerator::Notify, IWMReaderAcceleratorNotify, Notify, Notify method [windows Media Format], Notify method [windows Media Format],IWMReaderAccelerator interface, wmformat.iwmreaderaccelerator_notify, wmsdkidl/IWMReaderAccelerator::Notify
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
 - IWMReaderAccelerator.Notify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAccelerator::Notify


## -description



The <b>Notify</b> method is called by the source filter to pass in the negotiated media type.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> that specifies the stream associated with the notification.


### -param pSubtype [in]

Pointer to a media type that describes the current connection parameters for the stream.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code .




## -remarks



This method enables the reader to update its internal variables and commit to the DirectX VA connection. This is the last place the decoder or reader can fail.




## -see-also




<a href="https://msdn.microsoft.com/5cb2f564-88e3-4b60-bde3-6ccf69c97c48">Enabling DirectX Video Acceleration</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd757426(v=VS.85).aspx">IWMReaderAccelerator Interface</a>
 

 


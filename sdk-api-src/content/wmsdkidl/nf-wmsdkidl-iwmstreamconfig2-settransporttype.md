---
UID: NF:wmsdkidl.IWMStreamConfig2.SetTransportType
title: IWMStreamConfig2::SetTransportType
author: windows-sdk-content
description: The SetTransportType method sets the type of data communication protocol (reliable or unreliable) used for the stream.
old-location: wmformat\iwmstreamconfig2_settransporttype.htm
tech.root: wmformat
ms.assetid: 89958c80-2140-49ab-b696-189e8f722e96
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IWMStreamConfig2 interface [windows Media Format],SetTransportType method, IWMStreamConfig2.SetTransportType, IWMStreamConfig2::SetTransportType, IWMStreamConfig2SetTransportType, SetTransportType, SetTransportType method [windows Media Format], SetTransportType method [windows Media Format],IWMStreamConfig2 interface, wmformat.iwmstreamconfig2_settransporttype, wmsdkidl/IWMStreamConfig2::SetTransportType
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
 - IWMStreamConfig2.SetTransportType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMStreamConfig2::SetTransportType


## -description



The <b>SetTransportType</b> method sets the type of data communication protocol (reliable or unreliable) used for the stream.




## -parameters




### -param nTransportType [in]

One member of the <a href="https://msdn.microsoft.com/1d689487-f71b-4b27-928c-c55bd22579ed">WMT_TRANSPORT_TYPE</a> enumeration type specifying the transport type for the stream.


## -returns



The method always returns S_OK.




## -remarks



The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/dfe7b285-8d1d-4b71-a839-1c73d76e6444">IWMStreamConfig2::GetTransportType</a>
 

 


---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnTime
title: IWMReaderCallbackAdvanced::OnTime method
author: windows-driver-content
description: The OnTime method notifies the application of the clock time the reader is working to. This method is used when a user-provided clock has been specified.
old-location: wmformat\iwmreadercallbackadvanced_ontime.htm
old-project: wmformat
ms.assetid: 9913bbc4-df59-484f-b050-324e2ecdeb1c
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMReaderCallbackAdvanced, IWMReaderCallbackAdvanced interface [windows Media Format], OnTime method, IWMReaderCallbackAdvanced::OnTime, IWMReaderCallbackAdvancedOnTime, OnTime method [windows Media Format], OnTime method [windows Media Format], IWMReaderCallbackAdvanced interface, OnTime,IWMReaderCallbackAdvanced.OnTime, wmformat.iwmreadercallbackadvanced_ontime, wmsdkidl/IWMReaderCallbackAdvanced::OnTime
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmsdkidl.h
api_name:
-	IWMReaderCallbackAdvanced.OnTime
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderCallbackAdvanced::OnTime method


## -description



The <b>OnTime</b> method notifies the application of the clock time the reader is working to. This method is used when a user-provided clock has been specified.




## -parameters




### -param cnsCurrentTime [in]

<b>QWORD</b> containing the current time in 100-nanosecond units.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



There are two cases in which callbacks indicating what the reader registers as the current elapsed time must be received by an application. The first case occurs when there are gaps in an ASF file (for example, no audio for 10 seconds). The <b>OnTime</b> method continues to be called, while <a href="https://msdn.microsoft.com/0f6e4d4f-4295-44ff-95bc-e683bdbab8e0">OnSample</a> does not. In the second case, if the application is driving the clock, the reader calls <b>OnTime</b> after it has delivered all the data up to the point requested by the application in a call to <a href="https://msdn.microsoft.com/5e47ef96-9971-47b0-a003-b38f4045da7a">IWMReaderAdvanced::DeliverTime</a>.




## -see-also




<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>
 

 


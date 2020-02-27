---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnTime
title: IWMReaderCallbackAdvanced::OnTime (wmsdkidl.h)
description: The OnTime method notifies the application of the clock time the reader is working to. This method is used when a user-provided clock has been specified.
old-location: wmformat\iwmreadercallbackadvanced_ontime.htm
tech.root: wmformat
ms.assetid: 9913bbc4-df59-484f-b050-324e2ecdeb1c
ms.date: 12/05/2018
ms.keywords: IWMReaderCallbackAdvanced interface [windows Media Format],OnTime method, IWMReaderCallbackAdvanced.OnTime, IWMReaderCallbackAdvanced::OnTime, IWMReaderCallbackAdvancedOnTime, OnTime, OnTime method [windows Media Format], OnTime method [windows Media Format],IWMReaderCallbackAdvanced interface, wmformat.iwmreadercallbackadvanced_ontime, wmsdkidl/IWMReaderCallbackAdvanced::OnTime
f1_keywords:
- wmsdkidl/IWMReaderCallbackAdvanced.OnTime
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wmsdkidl.h
api_name:
- IWMReaderCallbackAdvanced.OnTime
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderCallbackAdvanced::OnTime


## -description



The <b>OnTime</b> method notifies the application of the clock time the reader is working to. This method is used when a user-provided clock has been specified.




## -parameters




### -param cnsCurrentTime [in]

<b>QWORD</b> containing the current time in 100-nanosecond units.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-start">IWMReader::Start</a> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://docs.microsoft.com/windows/desktop/wmformat/error-codes">Error Codes</a>.




## -remarks



There are two cases in which callbacks indicating what the reader registers as the current elapsed time must be received by an application. The first case occurs when there are gaps in an ASF file (for example, no audio for 10 seconds). The <b>OnTime</b> method continues to be called, while <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">OnSample</a> does not. In the second case, if the application is driving the clock, the reader calls <b>OnTime</b> after it has delivered all the data up to the point requested by the application in a call to <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime">IWMReaderAdvanced::DeliverTime</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced">IWMReaderCallbackAdvanced Interface</a>
 

 


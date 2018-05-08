---
UID: NF:wmsdkidl.IWMReaderAdvanced.DeliverTime
title: IWMReaderAdvanced::DeliverTime
author: windows-driver-content
description: The DeliverTime method provides the reader with a clock time. Use this method only when the application is providing the clock.
old-location: wmformat\iwmreaderadvanced_delivertime.htm
old-project: wmformat
ms.assetid: 5e47ef96-9971-47b0-a003-b38f4045da7a
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: DeliverTime, DeliverTime method [windows Media Format], DeliverTime method [windows Media Format],IWMReaderAdvanced interface, DeliverTime method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced interface [windows Media Format],DeliverTime method, IWMReaderAdvanced.DeliverTime, IWMReaderAdvanced2 interface [windows Media Format],DeliverTime method, IWMReaderAdvanced2::DeliverTime, IWMReaderAdvanced::DeliverTime, IWMReaderAdvancedDeliverTime, wmformat.iwmreaderadvanced_delivertime, wmsdkidl/IWMReaderAdvanced2::DeliverTime, wmsdkidl/IWMReaderAdvanced::DeliverTime
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
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
-	qasf.dll
api_name:
-	IWMReaderAdvanced.DeliverTime
-	IWMReaderAdvanced2.DeliverTime
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMReaderAdvanced::DeliverTime


## -description



The <b>DeliverTime</b> method provides the reader with a clock time. Use this method only when the application is providing the clock.




## -parameters




### -param cnsTime [in]

The time, in 100-nanosecond units.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>
 




## -remarks



Before making the first call to this method, call the <a href="https://msdn.microsoft.com/1f29beea-1da4-41e0-a68d-93af3b1f55ed">IWMReaderAdvanced::SetUserProvidedClock</a> method with the value <b>TRUE</b>, to specify that the application is providing the clock. Otherwise, the <b>DeliverTime</b> method returns E_UNEXPECTED.

After <b>DeliverTime</b> is called, the reader reads data as fast as possible until it reaches the specified time. When the reader reaches that time, it calls <a href="https://msdn.microsoft.com/9913bbc4-df59-484f-b050-324e2ecdeb1c">IWMReaderCallbackAdvanced::OnTime</a>, and then sends samples to the callback.

In general, the value of <i>cnsTime</i> should increase each time the method is called (that is, the clock should run forward). However, sometimes it may be possible to pass a smaller value. The <b>DeliverTime</b> method is asynchronous, meaning the reader object reads the data on another thread. The application can specify a smaller time value only if the reader object has not reached that point in the file. For example, if the application calls <b>DeliverTime</b> with the value 100 seconds, and immediately calls it again with the value 50 seconds, the call would probably succeed, because the reader object will not reach the 50-second point in the file. However, you cannot be sure the call will succeed in this case, because the application does not control the reader's thread.




## -see-also




<a href="https://msdn.microsoft.com/1b04f361-8147-4f6a-8c9d-d8eeed28550a">Broadcasting ASF Data</a>



<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2</a>
 

 


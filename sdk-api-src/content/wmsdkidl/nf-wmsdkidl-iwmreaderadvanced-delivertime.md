---
UID: NF:wmsdkidl.IWMReaderAdvanced.DeliverTime
title: IWMReaderAdvanced::DeliverTime (wmsdkidl.h)
description: The DeliverTime method provides the reader with a clock time. Use this method only when the application is providing the clock.
helpviewer_keywords: ["DeliverTime","DeliverTime method [windows Media Format]","DeliverTime method [windows Media Format]","IWMReaderAdvanced interface","DeliverTime method [windows Media Format]","IWMReaderAdvanced2 interface","IWMReaderAdvanced interface [windows Media Format]","DeliverTime method","IWMReaderAdvanced.DeliverTime","IWMReaderAdvanced2 interface [windows Media Format]","DeliverTime method","IWMReaderAdvanced2::DeliverTime","IWMReaderAdvanced::DeliverTime","IWMReaderAdvancedDeliverTime","wmformat.iwmreaderadvanced_delivertime","wmsdkidl/IWMReaderAdvanced2::DeliverTime","wmsdkidl/IWMReaderAdvanced::DeliverTime"]
old-location: wmformat\iwmreaderadvanced_delivertime.htm
tech.root: wmformat
ms.assetid: 5e47ef96-9971-47b0-a003-b38f4045da7a
ms.date: 4/26/2023
ms.keywords: DeliverTime, DeliverTime method [windows Media Format], DeliverTime method [windows Media Format],IWMReaderAdvanced interface, DeliverTime method [windows Media Format],IWMReaderAdvanced2 interface, IWMReaderAdvanced interface [windows Media Format],DeliverTime method, IWMReaderAdvanced.DeliverTime, IWMReaderAdvanced2 interface [windows Media Format],DeliverTime method, IWMReaderAdvanced2::DeliverTime, IWMReaderAdvanced::DeliverTime, IWMReaderAdvancedDeliverTime, wmformat.iwmreaderadvanced_delivertime, wmsdkidl/IWMReaderAdvanced2::DeliverTime, wmsdkidl/IWMReaderAdvanced::DeliverTime
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMReaderAdvanced::DeliverTime
 - wmsdkidl/IWMReaderAdvanced::DeliverTime
dev_langs:
 - c++
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
 - qasf.dll
api_name:
 - IWMReaderAdvanced.DeliverTime
 - IWMReaderAdvanced2.DeliverTime
---

# IWMReaderAdvanced::DeliverTime


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

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

Before making the first call to this method, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock">IWMReaderAdvanced::SetUserProvidedClock</a> method with the value <b>TRUE</b>, to specify that the application is providing the clock. Otherwise, the <b>DeliverTime</b> method returns E_UNEXPECTED.

After <b>DeliverTime</b> is called, the reader reads data as fast as possible until it reaches the specified time. When the reader reaches that time, it calls <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime">IWMReaderCallbackAdvanced::OnTime</a>, and then sends samples to the callback.

In general, the value of <i>cnsTime</i> should increase each time the method is called (that is, the clock should run forward). However, sometimes it may be possible to pass a smaller value. The <b>DeliverTime</b> method is asynchronous, meaning the reader object reads the data on another thread. The application can specify a smaller time value only if the reader object has not reached that point in the file. For example, if the application calls <b>DeliverTime</b> with the value 100 seconds, and immediately calls it again with the value 50 seconds, the call would probably succeed, because the reader object will not reach the 50-second point in the file. However, you cannot be sure the call will succeed in this case, because the application does not control the reader's thread.

## -see-also

<a href="/windows/desktop/wmformat/broadcasting-asf-data">Broadcasting ASF Data</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2">IWMReaderAdvanced2</a>
---
UID: NF:wmsdkidl.IWMReaderAdvanced.SetUserProvidedClock
title: IWMReaderAdvanced::SetUserProvidedClock (wmsdkidl.h)
description: The SetUserProvidedClock method specifies whether a clock provided by the application is to be used.
helpviewer_keywords: ["IWMReaderAdvanced interface [windows Media Format]","SetUserProvidedClock method","IWMReaderAdvanced.SetUserProvidedClock","IWMReaderAdvanced::SetUserProvidedClock","IWMReaderAdvancedSetUserProvidedClock","SetUserProvidedClock","SetUserProvidedClock method [windows Media Format]","SetUserProvidedClock method [windows Media Format]","IWMReaderAdvanced interface","wmformat.iwmreaderadvanced_setuserprovidedclock","wmsdkidl/IWMReaderAdvanced::SetUserProvidedClock"]
old-location: wmformat\iwmreaderadvanced_setuserprovidedclock.htm
tech.root: wmformat
ms.assetid: 1f29beea-1da4-41e0-a68d-93af3b1f55ed
ms.date: 12/05/2018
ms.keywords: IWMReaderAdvanced interface [windows Media Format],SetUserProvidedClock method, IWMReaderAdvanced.SetUserProvidedClock, IWMReaderAdvanced::SetUserProvidedClock, IWMReaderAdvancedSetUserProvidedClock, SetUserProvidedClock, SetUserProvidedClock method [windows Media Format], SetUserProvidedClock method [windows Media Format],IWMReaderAdvanced interface, wmformat.iwmreaderadvanced_setuserprovidedclock, wmsdkidl/IWMReaderAdvanced::SetUserProvidedClock
f1_keywords:
- wmsdkidl/IWMReaderAdvanced.SetUserProvidedClock
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
- IWMReaderAdvanced.SetUserProvidedClock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::SetUserProvidedClock


## -description



The <b>SetUserProvidedClock</b> method specifies whether a clock provided by the application is to be used.




## -parameters




### -param fUserClock [in]

Boolean value that is True if an application-provided clock is to be used.


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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The reader is not properly configured to handle this request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unable to set an internal event.

</td>
</tr>
</table>
 




## -remarks



In some cases, an application built on this SDK requires the clock to be driven by the application rather than by real time. This is true, for example, if the application reads from a file at a rate faster than it takes to play the file. User-provided clocks are only supported when the source file is a local file.

This method can fail if the current source does not support user-provided clocks. To drive a clock, an application must call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime">DeliverTime</a>, and then wait for <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime">IWMReaderCallbackAdvanced::OnTime</a> to reach the time specified.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getuserprovidedclock">IWMReaderAdvanced::GetUserProvidedClock</a>
 

 


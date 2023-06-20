---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetUserProvidedClock
title: IWMReaderAdvanced::GetUserProvidedClock (wmsdkidl.h)
description: The GetUserProvidedClock method ascertains whether a user-provided clock has been specified.
helpviewer_keywords: ["GetUserProvidedClock","GetUserProvidedClock method [windows Media Format]","GetUserProvidedClock method [windows Media Format]","IWMReaderAdvanced interface","IWMReaderAdvanced interface [windows Media Format]","GetUserProvidedClock method","IWMReaderAdvanced.GetUserProvidedClock","IWMReaderAdvanced::GetUserProvidedClock","IWMReaderAdvancedGetUserProvidedClock","wmformat.iwmreaderadvanced_getuserprovidedclock","wmsdkidl/IWMReaderAdvanced::GetUserProvidedClock"]
old-location: wmformat\iwmreaderadvanced_getuserprovidedclock.htm
tech.root: wmformat
ms.assetid: 54eb30ae-4b84-489c-a5e5-e73dee2c5056
ms.date: 4/26/2023
ms.keywords: GetUserProvidedClock, GetUserProvidedClock method [windows Media Format], GetUserProvidedClock method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetUserProvidedClock method, IWMReaderAdvanced.GetUserProvidedClock, IWMReaderAdvanced::GetUserProvidedClock, IWMReaderAdvancedGetUserProvidedClock, wmformat.iwmreaderadvanced_getuserprovidedclock, wmsdkidl/IWMReaderAdvanced::GetUserProvidedClock
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
 - IWMReaderAdvanced::GetUserProvidedClock
 - wmsdkidl/IWMReaderAdvanced::GetUserProvidedClock
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
api_name:
 - IWMReaderAdvanced.GetUserProvidedClock
---

# IWMReaderAdvanced::GetUserProvidedClock


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetUserProvidedClock</b> method ascertains whether a user-provided clock has been specified.

## -parameters

### -param pfUserClock [out]

Pointer to a Boolean value that is set to True if a user-provided clock has been specified.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfUserClock</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock">IWMReaderAdvanced::SetUserProvidedClock</a>
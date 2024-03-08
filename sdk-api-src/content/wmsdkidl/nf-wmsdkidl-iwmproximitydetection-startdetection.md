---
UID: NF:wmsdkidl.IWMProximityDetection.StartDetection
title: IWMProximityDetection::StartDetection (wmsdkidl.h)
description: The StartDetection method begins the proximity detection process. After calling this method, do not release the IWMProximityDetection until you receive the WMT_PROXIMITY_COMPLETED message.
helpviewer_keywords: ["IWMProximityDetection interface [windows Media Format]","StartDetection method","IWMProximityDetection.StartDetection","IWMProximityDetection::StartDetection","IWMProximityDetectionStartDetection","StartDetection","StartDetection method [windows Media Format]","StartDetection method [windows Media Format]","IWMProximityDetection interface","wmformat.iwmproximitydetection_startdetection","wmsdkidl/IWMProximityDetection::StartDetection"]
old-location: wmformat\iwmproximitydetection_startdetection.htm
tech.root: wmformat
ms.assetid: 90db4712-cf3e-4526-b07b-ea74c521dbc3
ms.date: 4/26/2023
ms.keywords: IWMProximityDetection interface [windows Media Format],StartDetection method, IWMProximityDetection.StartDetection, IWMProximityDetection::StartDetection, IWMProximityDetectionStartDetection, StartDetection, StartDetection method [windows Media Format], StartDetection method [windows Media Format],IWMProximityDetection interface, wmformat.iwmproximitydetection_startdetection, wmsdkidl/IWMProximityDetection::StartDetection
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMProximityDetection::StartDetection
 - wmsdkidl/IWMProximityDetection::StartDetection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMProximityDetection.StartDetection
---

# IWMProximityDetection::StartDetection


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>StartDetection</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>StartDetection</b> method begins the proximity detection process. After calling this method, do not release the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection</a> until you receive the WMT_PROXIMITY_COMPLETED message.

## -parameters

### -param pbRegistrationMsg [in]

Address of the registration message in memory. This message is received by your application from the device.

### -param cbRegistrationMsg [in]

Size of registration message in bytes.

### -param pbLocalAddress [in]

Address of a <b>SOCKADDR_STORAGE</b> structure that contains the address of the local network interface to be used during proximity detection. If the <i>dwExtraPortsAllowed</i> parameter is not 0, the port number specified in the SOCKADDR_STORAGE structure identifies the beginning of the range of ports that will be tried.

### -param cbLocalAddress [in]

Size of the structure pointed to by <i>pbLocalAddress</i>. Set to <code>sizeof(SOCKADDR_STORAGE)</code>.

### -param dwExtraPortsAllowed [in]

Specifies the number of additional ports that the method will attempt to use if the previous ports were not successfully used. The method always attempts to use the port specified in the <i>pbLocalAddress</i> parameter first. If that attempt fails, then the method makes a number of additional attempts up to the value of this parameter. On each subsequent attempt, the port number is incremented. So if the port number in <i>pbLocalAddress</i> is 5000, and <i>dwExtraPortsAllowed</i> is set to 20, the method will start with port 5000 and, if necessary, try ports 5001 through 5020.

### -param ppRegistrationResponseMsg [out]

Address of a variable that receives the address of the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface on the buffer object containing the registration response message. You must send this message data to the device.

### -param pCallback [in]

Address of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback">IWMStatusCallback</a> interface that will receive proximity detection status messages.

### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback. You can use this parameter to differentiate between messages from different objects when sharing a single status callback.

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
</table>

## -remarks

This method is asynchronous. When proximity detection is complete, a WMT_PROXIMITY_RESULT message is sent to the callback specified by <i>pCallback</i>. The completion message is accompanied by an <b>HRESULT</b> indicating success or failure.

Regardless of whether the proximity detection completes, the listening thread runs for two minutes, then send the  WMT_PROXIMITY_COMPLETED message. Do not release the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection</a> interface until you receive this message.

If this method returns a failure code, no messages are sent to the callback.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection Interface</a>
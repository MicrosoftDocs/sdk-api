---
UID: NF:wmsdkidl.IWMProximityDetection.StartDetection
title: IWMProximityDetection::StartDetection
author: windows-sdk-content
description: The StartDetection method begins the proximity detection process. After calling this method, do not release the IWMProximityDetection until you recieve the WMT_PROXIMITY_COMPLETED message.
old-location: wmformat\iwmproximitydetection_startdetection.htm
old-project: wmformat
ms.assetid: 90db4712-cf3e-4526-b07b-ea74c521dbc3
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IWMProximityDetection interface [windows Media Format],StartDetection method, IWMProximityDetection.StartDetection, IWMProximityDetection::StartDetection, IWMProximityDetectionStartDetection, StartDetection, StartDetection method [windows Media Format], StartDetection method [windows Media Format],IWMProximityDetection interface, wmformat.iwmproximitydetection_startdetection, wmsdkidl/IWMProximityDetection::StartDetection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProximityDetection::StartDetection


## -description


<p class="CCE_Message">[<b>StartDetection</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>StartDetection</b> method begins the proximity detection process. After calling this method, do not release the <a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection</a> until you recieve the WMT_PROXIMITY_COMPLETED message.




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

Address of a variable that receives the address of the <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface on the buffer object containing the registration response message. You must send this message data to the device.


### -param pCallback [in]

Address of the <a href="https://msdn.microsoft.com/a8d8eed8-0a87-40ce-b1bf-2d476c2e4ae3">IWMStatusCallback</a> interface that will receive proximity detection status messages.


### -param pvContext [in]

Generic pointer, for use by the application. This is passed to the application in calls to the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback. You can use this parameter to differentiate between messages from different objects when sharing a single status callback.


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

Regardless of whether the proximity detection completes, the listening thread runs for two minutes, then send the  WMT_PROXIMITY_COMPLETED message. Do not release the <a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection</a> interface until you receive this message.

If this method returns a failure code, no messages are sent to the callback.




## -see-also




<a href="https://msdn.microsoft.com/0897ad8f-8e06-4de9-840e-1588e0e20c54">IWMProximityDetection Interface</a>
 

 


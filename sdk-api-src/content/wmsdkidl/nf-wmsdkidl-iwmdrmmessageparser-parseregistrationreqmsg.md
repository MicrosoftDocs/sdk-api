---
UID: NF:wmsdkidl.IWMDRMMessageParser.ParseRegistrationReqMsg
title: IWMDRMMessageParser::ParseRegistrationReqMsg
author: windows-sdk-content
description: The ParseRegistrationReqMsg method extracts the device certificate and identifier from a registration message sent by a device.
old-location: wmformat\iwmdrmmessageparser_parseregistrationreqmsg.htm
old-project: wmformat
ms.assetid: d2d142bf-0fed-42c8-a2f1-b539a40ac074
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMDRMMessageParser interface [windows Media Format],ParseRegistrationReqMsg method, IWMDRMMessageParser.ParseRegistrationReqMsg, IWMDRMMessageParser::ParseRegistrationReqMsg, IWMDRMMessageParserParseRegistrationReqMsg, ParseRegistrationReqMsg, ParseRegistrationReqMsg method [windows Media Format], ParseRegistrationReqMsg method [windows Media Format],IWMDRMMessageParser interface, wmformat.iwmdrmmessageparser_parseregistrationreqmsg, wmsdkidl/IWMDRMMessageParser::ParseRegistrationReqMsg
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMDRMMessageParser.ParseRegistrationReqMsg
product: Windows
targetos: Windows
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMMessageParser::ParseRegistrationReqMsg


## -description


<p class="CCE_Message">[<b>ParseRegistrationReqMsg</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>ParseRegistrationReqMsg</b> method extracts the device certificate and identifier from a registration message sent by a device.




## -parameters




### -param pbRegistrationReqMsg [in]

Address of the registration message in memory. This is a message received by your application from a device.


### -param cbRegistrationReqMsg [in]

The size of registration message in bytes.


### -param ppDeviceCert [out]

Address of a variable that receives the address of the <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface of the buffer object that contains the device certificate.


### -param pDeviceSerialNumber [out]

Address of a <a href="https://msdn.microsoft.com/8981042a-f11d-458d-be27-3b1749f9e995">DRM_VAL16</a> structure that receives the device identifier.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbRegistrationMsg</i> parameter is <b>NULL</b>, or the <i>cbRegistrationMsg</i> parameter is 0.

</td>
</tr>
</table>
 




## -remarks



Registration request messages are sent by devices when they are connected to a network shared by the computer running your application. When your application receives the message, it must first parse the message by using this method to retrieve the device certificate and device identifier. The combination of device certificate and device identifier uniquely identifies the device.

After parsing the message with this method, you can search the device database to determine whether the device is already registered, or you can try to register the device. Both of these actions use the methods of the <a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/76e504e2-5978-4afd-9556-68f78c49a313">IWMDRMMessageParser Interface</a>
 

 


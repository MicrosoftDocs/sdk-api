---
UID: NF:mfidl.IMFNetSchemeHandlerConfig.GetSupportedProtocolType
title: IMFNetSchemeHandlerConfig::GetSupportedProtocolType
author: windows-sdk-content
description: Retrieves a supported protocol by index.
old-location: mf\imfnetschemehandlerconfig_getsupportedprotocoltype.htm
old-project: medfound
ms.assetid: 51cd90cf-a3ae-45dd-bc27-c91d44cab9f5
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 51cd90cf-a3ae-45dd-bc27-c91d44cab9f5, GetSupportedProtocolType, GetSupportedProtocolType method [Media Foundation], GetSupportedProtocolType method [Media Foundation],IMFNetSchemeHandlerConfig interface, IMFNetSchemeHandlerConfig interface [Media Foundation],GetSupportedProtocolType method, IMFNetSchemeHandlerConfig.GetSupportedProtocolType, IMFNetSchemeHandlerConfig::GetSupportedProtocolType, mf.imfnetschemehandlerconfig_getsupportedprotocoltype, mfidl/IMFNetSchemeHandlerConfig::GetSupportedProtocolType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFNetSchemeHandlerConfig.GetSupportedProtocolType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFNetSchemeHandlerConfig::GetSupportedProtocolType


## -description



Retrieves a supported protocol by index




## -parameters




### -param nProtocolIndex [in]

Zero-based index of the protocol to retrieve. To get the number of supported protocols, call <a href="https://msdn.microsoft.com/a0cbb01c-c86c-4186-81ca-6055aab5d361">IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols</a>.


### -param pnProtocolType [out]

Receives a member of the <a href="https://msdn.microsoft.com/dd628b9e-3c52-4c14-aa0f-5e0b811d3f57">MFNETSOURCE_PROTOCOL_TYPE</a> enumeration.


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
The value passed in the <i>nProtocolIndex</i> parameter was greater than the total number of supported protocols, returned by <a href="https://msdn.microsoft.com/a0cbb01c-c86c-4186-81ca-6055aab5d361">GetNumberOfSupportedProtocols</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/91bdcdbd-d621-42e3-8e0f-f8eeab489d35">IMFNetSchemeHandlerConfig</a>
 

 


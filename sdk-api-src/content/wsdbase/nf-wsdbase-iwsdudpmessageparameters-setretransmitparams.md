---
UID: NF:wsdbase.IWSDUdpMessageParameters.SetRetransmitParams
title: IWSDUdpMessageParameters::SetRetransmitParams
author: windows-sdk-content
description: Sets the values that WSD uses to determine how often to repeat the message transmission.
old-location: ncd\iwsdudpmessageparameters_setretransmitparams.htm
old-project: WsdApi
ms.assetid: 8fef8dc9-7621-4928-94a6-491a095b11fa
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: IWSDUdpMessageParameters interface,SetRetransmitParams method, IWSDUdpMessageParameters.SetRetransmitParams, IWSDUdpMessageParameters::SetRetransmitParams, SetRetransmitParams, SetRetransmitParams method, SetRetransmitParams method,IWSDUdpMessageParameters interface, ncd.iwsdudpmessageparameters_setretransmitparams, wsdbase/IWSDUdpMessageParameters::SetRetransmitParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsdbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSD_CONFIG_PARAM_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wsdapi.dll
api_name:
-	IWSDUdpMessageParameters.SetRetransmitParams
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDUdpMessageParameters::SetRetransmitParams


## -description


Sets the values that WSD uses to determine how often to repeat the message transmission.


## -parameters




### -param pParams [in]

Pointer to a <a href="https://msdn.microsoft.com/41bf73d8-0b20-4c38-b8b4-85c39eff0d91">WSDUdpRetransmitParams</a> structure. The structure contains values that determine how often WSD repeats the message transmission. 


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
</table>
 




## -remarks



If you do not specify these values, WSD sends the message only once.




## -see-also




<a href="https://msdn.microsoft.com/3af6e0ff-c0b9-47af-b018-37567f614adc">IWSDUdpMessageParameters</a>
 

 


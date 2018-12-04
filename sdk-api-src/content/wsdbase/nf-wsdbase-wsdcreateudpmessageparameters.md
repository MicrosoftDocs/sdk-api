---
UID: NF:wsdbase.WSDCreateUdpMessageParameters
title: WSDCreateUdpMessageParameters function
author: windows-sdk-content
description: Retrieves a pointer to the IWSDUdpMessageParameters interface.
old-location: ncd\wsdcreateudpmessageparameters.htm
tech.root: wsdapi
ms.assetid: a183a5f8-edd9-4881-84d4-b23701c40f36
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: WSDCreateUdpMessageParameters, WSDCreateUdpMessageParameters function, ncd.wsdcreateudpmessageparameters, wsdbase/WSDCreateUdpMessageParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wsdbase.h
req.include-header: Wsdapi.h
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
req.lib: Wsdapi.lib
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wsdapi.dll
api_name:
 - WSDCreateUdpMessageParameters
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WSDCreateUdpMessageParameters function


## -description


Retrieves a pointer to the <a href="https://msdn.microsoft.com/3af6e0ff-c0b9-47af-b018-37567f614adc">IWSDUdpMessageParameters</a> interface.


## -parameters




### -param ppTxParams [out]

Pointer to the <a href="https://msdn.microsoft.com/3af6e0ff-c0b9-47af-b018-37567f614adc">IWSDUdpMessageParameters</a> interface that you use to specify how often WSD repeats the message transmission.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>ppTxParams</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




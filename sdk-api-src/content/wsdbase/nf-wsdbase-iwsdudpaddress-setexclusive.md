---
UID: NF:wsdbase.IWSDUdpAddress.SetExclusive
title: IWSDUdpAddress::SetExclusive
author: windows-sdk-content
description: Controls whether the socket is in exclusive mode.
old-location: ncd\iwsdudpaddress_setexclusive.htm
old-project: WsdApi
ms.assetid: 08c5ee4a-55a4-4d8b-951e-d7faed45f44f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWSDUdpAddress interface,SetExclusive method, IWSDUdpAddress.SetExclusive, IWSDUdpAddress::SetExclusive, SetExclusive, SetExclusive method, SetExclusive method,IWSDUdpAddress interface, ncd.iwsdudpaddress_setexclusive, wsdbase/IWSDUdpAddress::SetExclusive
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsdbase.h
req.include-header: Wsdapi.h
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDUdpAddress.SetExclusive
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDUdpAddress::SetExclusive


## -description


Controls whether the socket is in exclusive mode.


## -parameters




### -param fExclusive [in]

A value of <b>TRUE</b> indicates that the socket should be set to exclusive mode. A value of <b>FALSE</b> indicates that the socket should not be in exclusive mode.


## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
 




## -see-also




<a href="https://msdn.microsoft.com/b666002f-2cd6-4e96-b055-34d801c1982e">IWSDUdpAddress</a>
 

 


---
UID: NF:upnp.IUPnPServices.get__NewEnum
title: IUPnPServices::get__NewEnum (upnp.h)
author: windows-sdk-content
description: The _NewEnum property specifies either the IEnumVARIANT or IEnumUnknown enumerator interface for the collection.
old-location: upnp\iupnpservices__newenum.htm
tech.root: upnp
ms.assetid: 8ca3156a-f33f-4fa4-b043-3ecde3f55d5d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUPnPServices interface [UPnP APIs],get__NewEnum method, IUPnPServices.get__NewEnum, IUPnPServices::get__NewEnum, _upnp_iupnpservices__newenum, get__NewEnum, get__NewEnum method [UPnP APIs], get__NewEnum method [UPnP APIs],IUPnPServices interface, upnp.iupnpservices__newenum, upnp/IUPnPServices::get__NewEnum
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPServices.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUPnPServices::get__NewEnum


## -description


The 
<b>_NewEnum</b> property specifies either the <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> or <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms683764">IEnumUnknown</a> enumerator interface for the collection.


## -parameters




### -param ppunk [out]

Receives a reference to the enumerator interface.


## -returns



For C++: If this property's "get" method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h, or one of the following UPnP-specific return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DOCUMENT_INVALID</b></dt>
</dl>
</td>
<td width="60%">
The service description contained an error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_EVENT_SUBSCRIPTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Failed to subscribe to the event source.

</td>
</tr>
</table>
 




## -remarks



This property is not visible in Visual Basic; use the <b>for...each...next</b> programming construct instead.




## -see-also




<a href="https://msdn.microsoft.com/8d5e487f-d2d4-4603-918c-e751d698be3c">IUPnPServices</a>
 

 


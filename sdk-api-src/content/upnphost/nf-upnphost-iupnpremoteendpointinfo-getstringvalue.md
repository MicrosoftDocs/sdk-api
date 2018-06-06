---
UID: NF:upnphost.IUPnPRemoteEndpointInfo.GetStringValue
title: IUPnPRemoteEndpointInfo::GetStringValue
author: windows-sdk-content
description: The GetStringValue method gets a string that provides information about either a request or requester.
old-location: upnp\iupnpremoteendpointinfo_getstringvalue.htm
old-project: UPnP
ms.assetid: c3b0dcd2-2195-4e09-aac4-073a3d848fa9
ms.author: windowssdkdev
ms.date: 04/25/2018
ms.keywords: GetStringValue, GetStringValue method [UPnP APIs], GetStringValue method [UPnP APIs],IUPnPRemoteEndpointInfo interface, IUPnPRemoteEndpointInfo interface [UPnP APIs],GetStringValue method, IUPnPRemoteEndpointInfo.GetStringValue, IUPnPRemoteEndpointInfo::GetStringValue, upnp.iupnpremoteendpointinfo_getstringvalue, upnphost/IUPnPRemoteEndpointInfo::GetStringValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: upnphost.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
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
tech.root: 
req.typenames: UI_EVENTPARAMS_COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPRemoteEndpointInfo.GetStringValue
product: Windows
targetos: Windows
req.lib: 
req.dll: Upnphost.dll
req.irql: 
req.product: Windows UI
---

# IUPnPRemoteEndpointInfo::GetStringValue


## -description


The <b>GetStringValue</b> method gets a string that provides information about either a request or requester.


## -parameters




### -param bstrValueName [in]

String that specifies the category of information to be retrieved.


### -param pbstrValue [out]

Pointer to a string, the meaning of which depends on the value of <i>bstrValueName</i>.

If <i>bstrValueName</i> is "RemoteAddress", the string is the requester's IP address.<b>Windows 7:  </b>To retrieve the HTTP UserAgent header, set <i>bstrValueName</i> to "HttpUserAgent".




## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



Currently, the only valid values for the <i>bstrValueName</i> parameter are "RemoteAddress" and (Windows 7 only) "HttpUserAgent". For any other value, this method will return the COM error code E_INVALIDARG.






## -see-also




<a href="https://msdn.microsoft.com/efbb0671-cb32-41e1-8405-1d145c247673">GetDwordValue</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff597612">GetGuidValue</a>



<a href="https://msdn.microsoft.com/32e246cd-50eb-4221-8166-a7cd8ed42d69">IUPnPRemoteEndpointInfo</a>
 

 


---
UID: NF:upnphost.IUPnPRemoteEndpointInfo.GetStringValue
title: IUPnPRemoteEndpointInfo::GetStringValue (upnphost.h)
description: The GetStringValue method gets a string that provides information about either a request or requester.
helpviewer_keywords: ["GetStringValue","GetStringValue method [UPnP APIs]","GetStringValue method [UPnP APIs]","IUPnPRemoteEndpointInfo interface","IUPnPRemoteEndpointInfo interface [UPnP APIs]","GetStringValue method","IUPnPRemoteEndpointInfo.GetStringValue","IUPnPRemoteEndpointInfo::GetStringValue","upnp.iupnpremoteendpointinfo_getstringvalue","upnphost/IUPnPRemoteEndpointInfo::GetStringValue"]
old-location: upnp\iupnpremoteendpointinfo_getstringvalue.htm
tech.root: upnp
ms.assetid: c3b0dcd2-2195-4e09-aac4-073a3d848fa9
ms.date: 12/05/2018
ms.keywords: GetStringValue, GetStringValue method [UPnP APIs], GetStringValue method [UPnP APIs],IUPnPRemoteEndpointInfo interface, IUPnPRemoteEndpointInfo interface [UPnP APIs],GetStringValue method, IUPnPRemoteEndpointInfo.GetStringValue, IUPnPRemoteEndpointInfo::GetStringValue, upnp.iupnpremoteendpointinfo_getstringvalue, upnphost/IUPnPRemoteEndpointInfo::GetStringValue
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
req.lib: 
req.dll: Upnphost.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPRemoteEndpointInfo::GetStringValue
 - upnphost/IUPnPRemoteEndpointInfo::GetStringValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnphost.dll
api_name:
 - IUPnPRemoteEndpointInfo.GetStringValue
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

<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpremoteendpointinfo-getdwordvalue">GetDwordValue</a>



<a href="/windows/desktop/api/upnphost/nf-upnphost-iupnpremoteendpointinfo-getguidvalue">GetGuidValue</a>



<a href="/windows/desktop/api/upnphost/nn-upnphost-iupnpremoteendpointinfo">IUPnPRemoteEndpointInfo</a>
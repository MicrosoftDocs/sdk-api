---
UID: NF:rtmv2.RtmCreateRouteListEnum
title: RtmCreateRouteListEnum function (rtmv2.h)
description: The RtmCreateRouteListEnum function creates an enumeration of routes on the specified route list.
helpviewer_keywords: ["RtmCreateRouteListEnum","RtmCreateRouteListEnum function [RAS]","_rtmv2ref_rtmcreateroutelistenum","rras.rtmcreateroutelistenum","rtmv2/RtmCreateRouteListEnum"]
old-location: rras\rtmcreateroutelistenum.htm
tech.root: RRAS
ms.assetid: 107fc253-58b3-479c-9cda-2c3b322e76f8
ms.date: 12/05/2018
ms.keywords: RtmCreateRouteListEnum, RtmCreateRouteListEnum function [RAS], _rtmv2ref_rtmcreateroutelistenum, rras.rtmcreateroutelistenum, rtmv2/RtmCreateRouteListEnum
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RtmCreateRouteListEnum
 - rtmv2/RtmCreateRouteListEnum
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmCreateRouteListEnum
---

# RtmCreateRouteListEnum function


## -description

The 
<b>RtmCreateRouteListEnum</b> function creates an enumeration of routes on the specified route list.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param RouteListHandle [in]

Handle to the route list to enumerate that is obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmcreateroutelist">RtmCreateRouteList</a>.

### -param RtmEnumHandle [out]

On input, <i>RtmEnumHandle</i> is a pointer to <b>NULL</b>. 




On output, <i>RtmEnumHandle</i> receives a pointer to a handle to the enumeration. Use this handle in all subsequent calls to functions that enumerate the list of routes.

## -returns

If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to complete this operation.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

When the enumeration handle is no longer required, release it by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>.

For sample code using this function, see 
<a href="/windows/desktop/RRAS/use-a-client-specific-route-list">Use a Client-Specific Route List</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetlistenumroutes">RtmGetListEnumRoutes</a>
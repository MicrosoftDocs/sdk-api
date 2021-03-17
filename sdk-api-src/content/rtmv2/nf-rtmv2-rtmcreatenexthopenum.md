---
UID: NF:rtmv2.RtmCreateNextHopEnum
title: RtmCreateNextHopEnum function (rtmv2.h)
description: The RtmCreateNextHopEnum enumerates the next hops in the next-hop list.
helpviewer_keywords: ["RTM_ENUM_NEXT","RTM_ENUM_RANGE","RTM_ENUM_START","RtmCreateNextHopEnum","RtmCreateNextHopEnum function [RAS]","_rtmv2ref_rtmcreatenexthopenum","rras.rtmcreatenexthopenum","rtmv2/RtmCreateNextHopEnum"]
old-location: rras\rtmcreatenexthopenum.htm
tech.root: RRAS
ms.assetid: d26ce475-ea05-4e84-92da-06df9c386858
ms.date: 12/05/2018
ms.keywords: RTM_ENUM_NEXT, RTM_ENUM_RANGE, RTM_ENUM_START, RtmCreateNextHopEnum, RtmCreateNextHopEnum function [RAS], _rtmv2ref_rtmcreatenexthopenum, rras.rtmcreatenexthopenum, rtmv2/RtmCreateNextHopEnum
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
 - RtmCreateNextHopEnum
 - rtmv2/RtmCreateNextHopEnum
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
 - RtmCreateNextHopEnum
---

# RtmCreateNextHopEnum function


## -description

The 
<b>RtmCreateNextHopEnum</b> enumerates the next hops in the next-hop list.

## -parameters

### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmregisterentity">RtmRegisterEntity</a>.

### -param EnumFlags [in]

Specifies which next hops to include in the enumeration. The following flags are used. 



<table>
<tr>
<th>Constant</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_NEXT"></a><a id="rtm_enum_next"></a><dl>
<dt><b>RTM_ENUM_NEXT</b></dt>
</dl>
</td>
<td width="60%">
Enumerate next hops starting at the specified address/mask length (such as 10/8). The enumeration continues to the end of the next hop list.

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_RANGE"></a><a id="rtm_enum_range"></a><dl>
<dt><b>RTM_ENUM_RANGE</b></dt>
</dl>
</td>
<td width="60%">
Enumerate next hops in the specified range specified by the address/mask length (such as 10/8).

</td>
</tr>
<tr>
<td width="40%"><a id="RTM_ENUM_START"></a><a id="rtm_enum_start"></a><dl>
<dt><b>RTM_ENUM_START</b></dt>
</dl>
</td>
<td width="60%">
Enumerate next hops starting at 0/0. Specify <b>NULL</b> for <i>NetAddress</i>.

</td>
</tr>
</table>

### -param NetAddress [in]

Pointer to an 
<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a> structure that contains the starting address of the enumeration. Specify <b>NULL</b> if <i>EnumFlags</i> contains RTM_ENUM_START.

### -param RtmEnumHandle [out]

On input, <i>RtmEnumHandle</i> is a pointer to <b>NULL</b>. 




On output, <i>RtmEnumHandle</i> receives a pointer to a handle to the enumeration. Use this handle in all subsequent calls to 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumnexthops">RtmGetEnumNextHops</a>, 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>, and 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contains incorrect information.

</td>
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

If <i>EnumFlags</i> contains RTM_ENUM_RANGE, use <i>NetAddress</i> to specify the range of the routing table to enumerate. For example, if a client sets <i>NetAddress</i> to 10/8, next hops in the range 10.0.0.0/8 to 10.255.255.255/32 are returned.

When the enumeration handle is no longer required, release it by calling 
<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>.

## -see-also

<a href="/windows/desktop/api/rtmv2/ns-rtmv2-rtm_net_address">RTM_NET_ADDRESS</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmdeleteenumhandle">RtmDeleteEnumHandle</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmgetenumnexthops">RtmGetEnumNextHops</a>



<a href="/windows/desktop/api/rtmv2/nf-rtmv2-rtmreleasenexthops">RtmReleaseNextHops</a>
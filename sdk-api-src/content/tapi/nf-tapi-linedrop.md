---
UID: NF:tapi.lineDrop
title: lineDrop function
author: windows-driver-content
description: The lineDrop function drops or disconnects the specified call. The application has the option to specify user-user information to be transmitted as part of the call disconnect.
old-location: tapi2\linedrop.htm
old-project: Tapi
ms.assetid: ce1f1dbb-287b-483a-9e7e-87af0d07e4e4
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: "_tapi2_linedrop, lineDrop, lineDrop function [TAPI 2.2], tapi/lineDrop, tapi2.linedrop"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	lineDrop
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# lineDrop function


## -description


The 
<b>lineDrop</b> function drops or disconnects the specified call. The application has the option to specify user-user information to be transmitted as part of the call disconnect.


## -parameters




### -param hCall

Handle to the call to be dropped. The application must be an owner of the call. The call state of <i>hCall</i> can be any state except <i>idle</i>.


### -param lpsUserUserInfo

Pointer to a string containing user-user information to be sent to the remote party as part of the call disconnect. This pointer can be left <b>NULL</b> if no user-user information is to be sent. User-user information is only sent if supported by the underlying network (see 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>). The protocol discriminator field for the user-user information, if required, should appear as the first byte of the buffer pointed to by <i>lpsUserUserInfo</i>, and must be accounted for in <i>dwSize</i>.


### -param dwSize

Size of the user-user information in <i>lpsUserUserInfo</i>, in bytes. If <i>lpsUserUserInfo</i> is <b>NULL</b>, no user-user information is sent to the calling party and <i>dwSize</i> is ignored.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_NOMEM, LINEERR_OPERATIONFAILED, LINEERR_NOTOWNER, LINEERR_RESOURCEUNAVAIL, LINEERR_INVALPOINTER, LINEERR_USERUSERINFOTOOBIG, LINEERR_INVALCALLSTATE, LINEERR_UNINITIALIZED.




## -remarks



When invoking 
<b>lineDrop</b>, related calls can sometimes be affected as well. For example, dropping a conference call can drop all individual participating calls. 
<a href="https://msdn.microsoft.com/7b24e3c3-bc69-488b-a698-cf17875bc3c5">LINE_CALLSTATE</a> messages are sent to the application for all calls whose call state is affected. A dropped call typically transitions to the <i>idle</i> state. Invoking 
<b>lineDrop</b> on a call in the <i>offering</i> state rejects the call. Not all telephone networks provide this capability.

A call in the <i>onholdpending</i> state typically reverts to the <i>connected</i> state. When dropping the consultation call to the third party for a conference call or when removing the third party in a previously established conference call, the provider (and switch) can release the conference bridge and revert the call back to a normal two-party call. If this is the case, <i>hConfCall</i> transitions to the <i>idle</i> state, and the only remaining participating call transitions to the <i>connected</i> state. Some switches automatically "unhold" the other call.

The application has the option to send user-user information at the time of the drop. Even if user-user information can be sent, there is no guarantee that the network will deliver this information to the remote party.

In various bridged or party-line configurations when multiple parties are on the call, 
<b>lineDrop</b> may not actually clear the call. For example, in a bridged situation, a 
<b>lineDrop</b> operation may not actually drop the call because the status of other stations on the call may govern; instead, the call may simply be changed to the LINECONNECTEDMODE_INACTIVE mode if it remains <i>connected</i> at other stations.




## -see-also




<a href="https://msdn.microsoft.com/dc348bb2-d564-40f8-afe3-5473c5769fa4">Drop overview</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>



<a href="https://msdn.microsoft.com/69ed2e2c-f1c7-4f69-86a0-3cfdd80e423d">Terminate a Session overview</a>
 

 


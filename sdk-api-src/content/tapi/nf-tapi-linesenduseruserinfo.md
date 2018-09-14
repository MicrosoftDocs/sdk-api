---
UID: NF:tapi.lineSendUserUserInfo
title: lineSendUserUserInfo function
author: windows-sdk-content
description: The lineSendUserUserInfo function sends user-user information to the remote party on the specified call.
old-location: tapi2\linesenduseruserinfo.htm
tech.root: TAPI
ms.assetid: 833827a0-bbb2-4df9-87a0-3b2eb1904611
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: "_tapi2_linesenduseruserinfo, lineSendUserUserInfo, lineSendUserUserInfo function [TAPI 2.2], tapi/lineSendUserUserInfo, tapi2.linesenduseruserinfo"
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSendUserUserInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# lineSendUserUserInfo function


## -description


 The 
<b>lineSendUserUserInfo</b> function sends user-user information to the remote party on the specified call.


## -parameters




### -param hCall

Handle to the call on which to send user-user information. The application must be an owner of the call. The call state of <i>hCall</i> must be <i>connected</i>, <i>offering</i>, <i>accepted</i>, or <i>ringback</i>.


### -param lpsUserUserInfo

Pointer to a string containing user-user information to be sent to the remote party. User-user information is only sent if supported by the underlying network (see 
<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>). The protocol discriminator field for the user-user information, if required, should appear as the first byte of the buffer pointed to by <i>lpsUserUserInfo</i>, and must be accounted for in <i>dwSize</i>.


### -param dwSize

Size of the user-user information in <i>lpsUserUserInfo</i>, in bytes.


## -returns



Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.




## -remarks



This function can be used to send user-user information at any time during a connected call. If the size of the specified information to be sent is larger than what can fit into a single network message (as in ISDN), the service provider is responsible for dividing the information into a sequence of chained network messages (using "more data").

User-user information can also be sent as part of call accept, call reject, and call redirect, and when making calls. User-user information can also be received. The received information is available through the call's call-information record. Whenever user-user information arrives after call offering or prior to call disconnect, a 
<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a> message with a <i>UserUserInfo</i> parameter notifies the application that user-user information in the call-information record has changed. If multiple network messages are chained, the information is assembled by the service provider and a single message is sent to the application.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://msdn.microsoft.com/83e38453-bb93-4cc5-923f-d0cd2898350a">LINEDEVCAPS</a>



<a href="https://msdn.microsoft.com/eb882409-6842-434e-9f93-61cf0c11d1d0">LINE_CALLINFO</a>



<a href="https://msdn.microsoft.com/5d98ed8b-b75e-49f8-aba3-c6eee89e91c1">LINE_REPLY</a>



<a href="https://msdn.microsoft.com/d4338b3c-cd84-4abb-b74e-9df895c8355b">Supplementary Line Service Functions</a>



<a href="https://msdn.microsoft.com/d703b414-1389-416c-8e94-c1931979f0c9">TAPI 2.2 Reference Overview</a>
 

 


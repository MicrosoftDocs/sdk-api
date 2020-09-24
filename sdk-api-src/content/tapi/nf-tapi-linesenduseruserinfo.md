---
UID: NF:tapi.lineSendUserUserInfo
title: lineSendUserUserInfo function (tapi.h)
description: The lineSendUserUserInfo function sends user-user information to the remote party on the specified call.
helpviewer_keywords: ["_tapi2_linesenduseruserinfo","lineSendUserUserInfo","lineSendUserUserInfo function [TAPI 2.2]","tapi/lineSendUserUserInfo","tapi2.linesenduseruserinfo"]
old-location: tapi2\linesenduseruserinfo.htm
tech.root: tapi3
ms.assetid: 833827a0-bbb2-4df9-87a0-3b2eb1904611
ms.date: 12/05/2018
ms.keywords: _tapi2_linesenduseruserinfo, lineSendUserUserInfo, lineSendUserUserInfo function [TAPI 2.2], tapi/lineSendUserUserInfo, tapi2.linesenduseruserinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineSendUserUserInfo
 - tapi/lineSendUserUserInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineSendUserUserInfo
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
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>). The protocol discriminator field for the user-user information, if required, should appear as the first byte of the buffer pointed to by <i>lpsUserUserInfo</i>, and must be accounted for in <i>dwSize</i>.

### -param dwSize

Size of the user-user information in <i>lpsUserUserInfo</i>, in bytes.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALCALLHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCALLSTATE, LINEERR_OPERATIONFAILED, LINEERR_INVALPOINTER, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_USERUSERINFOTOOBIG, LINEERR_NOTOWNER, LINEERR_UNINITIALIZED.

## -remarks

This function can be used to send user-user information at any time during a connected call. If the size of the specified information to be sent is larger than what can fit into a single network message (as in ISDN), the service provider is responsible for dividing the information into a sequence of chained network messages (using "more data").

User-user information can also be sent as part of call accept, call reject, and call redirect, and when making calls. User-user information can also be received. The received information is available through the call's call-information record. Whenever user-user information arrives after call offering or prior to call disconnect, a 
<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a> message with a <i>UserUserInfo</i> parameter notifies the application that user-user information in the call-information record has changed. If multiple network messages are chained, the information is assembled by the service provider and a single message is sent to the application.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>



<a href="/windows/desktop/Tapi/line-callinfo">LINE_CALLINFO</a>



<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>
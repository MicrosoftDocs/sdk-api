---
UID: NF:mi.MI_Context_GetLocalSession
title: MI_Context_GetLocalSession function (mi.h)
description: Gets the local session (MI_Session) which allows the provider to perform CIM operations against the local server hosting the provider.
old-location: wmi_v2\mi_context_getlocalsession.htm
tech.root: wmi_v2
ms.assetid: 275657b1-9e74-456e-9ef9-28b621d27fc7
ms.date: 12/05/2018
ms.keywords: MI_Context_GetLocalSession, MI_Context_GetLocalSession function [Windows Management Infrastructure (MI)], mi/MI_Context_GetLocalSession, wmi.mi_getlocalsession, wmi_v2.mi_context_getlocalsession
f1_keywords:
- mi/MI_Context_GetLocalSession
dev_langs:
- c++
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_Context_GetLocalSession
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_Context_GetLocalSession function


## -description


Gets the local session (<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_session">MI_Session</a>) which allows the provider to perform CIM operations against  the local server hosting the provider.


## -parameters




### -param context [in]

A pointer to the request context.


### -param session [out]

A pointer to the returned <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_session">MI_Session</a> object. This session must not be closed.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



This session is pre-instantiated and has the lifetime of the context from which the session was obtained. The provider must not close this session because its lifetime is bound to the context.

The provider should call this function rather than creating a new session through the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newsession">MI_Application_NewSession</a> function, because some optimizations may be possible for talking to the CIM server.

The security context used to call the <b>MI_Context_GetLocalSession</b> function should be the same identity used communicate back to the server through the MI_Session_* operation functions. Do not cache these sessions outside the current operation. The provider calls this method multiple times within an operation under different identities, in which case the retrieved session should also be used with the same identity. Any operations on the session should always be the same identity that the user retrieved for the local session, or else the operation could fail with the <b>MI_RESULT_ACCESS_DENIED</b> return code.




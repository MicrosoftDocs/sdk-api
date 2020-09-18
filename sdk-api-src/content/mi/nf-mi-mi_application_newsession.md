---
UID: NF:mi.MI_Application_NewSession
title: MI_Application_NewSession function (mi.h)
description: Creates a session used to share connections for a set of operations to a single destination.
helpviewer_keywords: ["MI_Application_NewSession","MI_Application_NewSession function [Windows Management Infrastructure (MI)]","mi/MI_Application_NewSession","wmi_v2.mi_application_newsession"]
old-location: wmi_v2\mi_application_newsession.htm
tech.root: wmi_v2
ms.assetid: 76010766-aa20-4632-940d-48d9769803da
ms.date: 12/05/2018
ms.keywords: MI_Application_NewSession, MI_Application_NewSession function [Windows Management Infrastructure (MI)], mi/MI_Application_NewSession, wmi_v2.mi_application_newsession
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
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_Application_NewSession
 - mi/MI_Application_NewSession
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Application_NewSession
---

# MI_Application_NewSession function


## -description

Creates a session used to share connections for a set of operations to a single destination.

## -parameters

### -param application [in]

A pointer to a handle returned from the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_initializev1">MI_Application_Initialize</a> function.

### -param protocol [in, optional]

A pointer to an optional protocol handler to carry out the operation.  If this parameter is <b>NULL</b>, a default value is used, based on the destination. Currently supported protocols are L"WMIDCOM" and L"WINRM".

### -param destination [in, optional]

An optional destination for the session. If the destination argument is <b>NULL</b>, the session communicates with the local machine. Otherwise, the destination can be the computer name of the local machine or a remote machine.

### -param options [in, optional]

A pointer to optional destination options, such as default time-outs and credentials.

### -param callbacks [in, optional]

A pointer to an optional MI_SessionCallbacks structure that contains callbacks to receive various results.

### -param extendedError

Pointer to optional additional error information if the operation failed.  When you have finished using the error information, free the memory by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_instance_delete">MI_Instance_Delete</a> function.

### -param session [out]

A pointer to the returned session handle.  When you have finished using the session handle, close it by calling the <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_session_close">MI_Session_Close</a> function. If the session handle is not closed before shutting down both the application and the application handle, the application handle shutdown will not respond.

## -returns

This function returns MI_INLINE MI_Result.

## -remarks

Creating a destination may not communicate with the destination computer. It will not be until the first operation is carried out on a session that the application can determine whether the computer is accessible.

The <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_session_close">MI_Session_Close</a> function must be called on the outbound session handle. Close all operations under the target session before closing the session.

If  no protocol is specified and <i>destination</i> is <b>NULL</b>, the WMIDCOM protocol is used. If no protocol is specified and <i>destination</i> is not <b>NULL</b>, the WINRM protocol is used. .

## -see-also

<a href="/windows/desktop/WinRM/portal">Windows Remote Management</a>
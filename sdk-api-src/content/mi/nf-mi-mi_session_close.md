---
UID: NF:mi.MI_Session_Close
title: MI_Session_Close function
author: windows-sdk-content
description: Closes a session and releases all associated memory.
old-location: wmi_v2\mi_session_close.htm
old-project: wmi_v2
ms.assetid: c77a93b0-446c-417b-81ab-746c639477f7
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: MI_Session_Close, MI_Session_Close function [Windows Management Infrastructure (MI)], mi/MI_Session_Close, wmi_v2.mi_session_close
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: MI_Type
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_Session_Close
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# MI_Session_Close function


## -description


Closes a session and releases all associated memory.


## -parameters




### -param session [in, out]

Session handle returned from <a href="https://msdn.microsoft.com/76010766-aa20-4632-940d-48d9769803da">MI_Application_NewSession</a>.


### -param completionContext [in, optional]

Optional parameter to be returned through the <b>completionCallback</b> callback.


### -param completionCallback [in, out]

Optional callback to make the session close asynchronous.  (If this value is <b>NULL</b>, then the close call is synchronous.) If the <b>MI_Session_Close</b> is called from a callback the completion callback must be specified.  Not doing so can result in a deadlock.



#### completionContext


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -remarks



Closing a session will cause all operations that are currently running to be canceled.  Canceling operations will cause asynchronous operation callbacks to be called (with the final result of an MI_Operation_Get* function call's <i>moreResults</i> parameter equal to <b>MI_FALSE</b>, although more than one result may be delivered before this happens).  Not closing all operation handles that were created with the current session will cause the closing of the session to stop responding for synchronous calls and the asynchronous callback will not be called.  Operation and session handles not fully closed will cause the application handle to stop responding during shutdown.




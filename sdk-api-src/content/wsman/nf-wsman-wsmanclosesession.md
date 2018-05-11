---
UID: NF:wsman.WSManCloseSession
title: WSManCloseSession function
author: windows-driver-content
description: Closes a session object.
old-location: winrm\wsmanclosesession.htm
old-project: WinRM
ms.assetid: b7d1ef66-0371-4d30-8053-813b229b2a62
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: WSManCloseSession, WSManCloseSession function [Windows Remote Management], winrm.wsmanclosesession, wsman/WSManCloseSession
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSManSessionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WsmSvc.dll
api_name:
-	WSManCloseSession
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManCloseSession function


## -description


Closes a session object.


## -parameters




### -param session [in, out, optional]

Specifies the session handle to close. This handle is returned by a <a href="https://msdn.microsoft.com/5123d876-5123-4fa4-8f6f-859a26aad825">WSManCreateSession</a> call.  This parameter cannot be NULL.


### -param flags

Reserved for future use.  Must be zero.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.




## -remarks



The <b>WSManCloseSession</b> method frees the memory associated with a session and closes all related operations before returning. This is a synchronous call.  All operations are explicitly canceled. It is recommended that all pending operations are either completed or explicitly canceled before calling this function.




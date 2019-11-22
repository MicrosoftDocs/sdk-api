---
UID: NF:wsman.WSManCloseSession
title: WSManCloseSession function (wsman.h)

description: Closes a session object.
old-location: winrm\wsmanclosesession.htm
tech.root: winrm
ms.assetid: b7d1ef66-0371-4d30-8053-813b229b2a62

ms.date: 12/05/2018
ms.keywords: WSManCloseSession, WSManCloseSession function [Windows Remote Management], winrm.wsmanclosesession, wsman/WSManCloseSession
ms.topic: function
f1_keywords: 
 - "wsman/WSManCloseSession"
dev_langs:
 - c++
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
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManCloseSession
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
---

# WSManCloseSession function


## -description


Closes a session object.


## -parameters




### -param session [in, out, optional]

Specifies the session handle to close. This handle is returned by a <a href="https://docs.microsoft.com/windows/desktop/api/wsman/nf-wsman-wsmancreatesession">WSManCreateSession</a> call.  This parameter cannot be NULL.


### -param flags

Reserved for future use.  Must be zero.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.




## -remarks



The <b>WSManCloseSession</b> method frees the memory associated with a session and closes all related operations before returning. This is a synchronous call.  All operations are explicitly canceled. It is recommended that all pending operations are either completed or explicitly canceled before calling this function.




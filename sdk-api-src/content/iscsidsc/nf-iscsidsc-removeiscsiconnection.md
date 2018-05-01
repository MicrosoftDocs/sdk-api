---
UID: NF:iscsidsc.RemoveIScsiConnection
title: RemoveIScsiConnection function
author: windows-driver-content
description: RemoveIscsiConnection function removes a connection from an active session.
old-location: iscsidisc\removeiscsiconnection.htm
old-project: iSCSIDisc
ms.assetid: 1d34348a-b16a-4420-88e1-092e3f521ea5
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: RemoveIScsiConnection, RemoveIscsiConnection, RemoveIscsiConnection function [iSCSI Discovery Library API], iscsidisc.removeiscsiconnection, iscsidsc/RemoveIscsiConnection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TARGET_INFORMATION_CLASS, *PTARGET_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iscsidsc.dll
api_name:
-	RemoveIscsiConnection
product: Windows
targetos: Windows
req.lib: Iscsidsc.lib
req.dll: Iscsidsc.dll
req.irql: 
req.product: GDI+ 1.1
---

# RemoveIScsiConnection function


## -description


The <b>RemoveIscsiConnection</b> function removes a connection from an active session.



## -parameters




### -param UniqueSessionId [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/d13975f9-58d0-425c-a2de-a0d1d70850d3">ISCSI_UNIQUE_SESSION_ID</a> that specifies the unique session identifier of the session that the connection belongs to.


### -param ConnectionId

TBD




#### - UniqueConnectionId [in]

A pointer to a structure of type <a href="https://msdn.microsoft.com/cc68fda4-6dbf-42de-8e0e-e144bd4e9524">ISCSI_UNIQUE_CONNECTION_ID</a> that specifies the connection to remove. 


## -returns



Returns ERROR_SUCCESS if the operation succeeds. Otherwise, it returns the appropriate Win32 or iSCSI error code.





## -remarks



The <b>RemoveIscsiConnection</b> function will not remove the last connection of a session or the leading connection of a session. The caller must close the session by calling <a href="https://msdn.microsoft.com/c49ad2e2-3f06-48e7-bf38-6074f9a6bcad">LogoutIscsiTarget</a> to remove the last connection.






## -see-also




<a href="https://msdn.microsoft.com/c49ad2e2-3f06-48e7-bf38-6074f9a6bcad">LogoutIscsiTarget</a>
 

 


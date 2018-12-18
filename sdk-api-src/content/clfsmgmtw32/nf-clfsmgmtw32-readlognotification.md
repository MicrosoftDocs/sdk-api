---
UID: NF:clfsmgmtw32.ReadLogNotification
title: ReadLogNotification function
author: windows-sdk-content
description: Retrieves notifications from the log manager. It retrieves a queued notification from the log manager immediately if a notification is available; otherwise the request remains pending until a notification is generated.
old-location: fs\readlognotification.htm
tech.root: Clfs
ms.assetid: 08931011-511b-471b-9a4a-ebc96e963c51
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ReadLogNotification, ReadLogNotification function [Files], clfsmgmtw32/ReadLogNotification, fs.readlognotification
ms.topic: function
req.header: clfsmgmtw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - ReadLogNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReadLogNotification function


## -description


The <b>ReadLogNotification</b> function retrieves notifications from the log manager. It retrieves a queued notification from the log manager immediately if a notification is available; otherwise the request remains pending until a notification is generated.  


## -parameters




### -param hLog [in]

The handle to the log. 


### -param pNotification [out]

Receives the notification type, and if the type has parameters associated with it, the parameters. 


### -param lpOverlapped [in]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that is required for asynchronous operation. If asynchronous operation is not used, this parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The following is a possible error code:




## -remarks



If the log handle is not created with the <b>FILE_FLAG_OVERLAPPED</b> file option, no operations can start on the log handle while the call to <b>ReadLogNotification</b>  is pending.




## -see-also




<a href="https://msdn.microsoft.com/ba7f7414-885f-40d0-ab61-2348d7f6125b">CLFS_MGMT_NOTIFICATION</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>
 

 


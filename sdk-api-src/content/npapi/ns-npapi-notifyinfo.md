---
UID: NS:npapi._NOTIFYINFO
title: NOTIFYINFO
author: windows-sdk-content
description: The NOTIFYINFO structure contains status information about a network connect or disconnect operation. It is used by the AddConnectNotify and CancelConnectNotify functions.
old-location: security\notifyinfo.htm
tech.root: secauthn
ms.assetid: 43b31128-da9c-470b-b030-0010b250a291
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPNOTIFYINFO, LPNOTIFYINFO, LPNOTIFYINFO structure pointer [Security], NOTIFYINFO, NOTIFYINFO structure [Security], _mnp_notifyinfo, npapi/LPNOTIFYINFO, npapi/NOTIFYINFO, security.notifyinfo"
ms.topic: struct
req.header: npapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Npapi.h
api_name:
 - NOTIFYINFO
product: Windows
targetos: Windows
req.typenames: NOTIFYINFO, *LPNOTIFYINFO
req.redist: 
---

# NOTIFYINFO structure


## -description


The <b>NOTIFYINFO</b> structure contains status information about a network connect or disconnect operation. It is used by the 
<a href="https://msdn.microsoft.com/a061b088-81ca-4276-a0d6-9f1d1282a039">AddConnectNotify</a> and 
<a href="https://msdn.microsoft.com/94bd969d-f94d-449c-971d-d17fff2c07e1">CancelConnectNotify</a> functions.


## -struct-fields




### -field dwNotifyStatus

This will be either NOTIFY_PRE or NOTIFY_POST to indicate whether this notification is sent before or after the connection or disconnection is performed.


### -field dwOperationStatus

This is set to WN_SUCCESS when <b>dwNotifyStatus</b> is NOTIFY_PRE. 




If <b>dwNotifyStatus</b> is set to NOTIFY_POST, <b>dwOperationStatus</b> contains the return status code from the function performing the operation: 
<a href="https://msdn.microsoft.com/37a3988c-18ee-400a-85c3-cc3cbdf015ea">NPAddConnection</a> or 
<a href="https://msdn.microsoft.com/e06768b2-760c-48f1-a6a4-896c3ea286f6">NPCancelConnection</a>.


### -field lpContext

Used by the application receiving the notification in order to keep a context for the operation between the pre-notification and the post-notification calls. In other words, it enables the notification application to match the advance notification call to the corresponding after-the-fact notification call for a particular event. The <b>lpContext</b> member is a <b>NULL</b> pointer when the notification function is called for advance notification. The notification function can return with <b>lpContext</b> still <b>NULL</b>, indicating that it is not interested in further notification for this specific operation. In this case, the notification function will not be called again with after-the-fact notification for this operation. If the advance notification function call returns a non-<b>NULL</b> value in <b>lpContext</b>, this value is passed in when the notification function is called for the after-the-fact notification for that same operation.


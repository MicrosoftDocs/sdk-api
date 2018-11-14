---
UID: NF:sbtsv.ITsSbResourceNotificationEx.NotifySessionChangeEx
title: ITsSbResourceNotificationEx::NotifySessionChangeEx
author: windows-sdk-content
description: Notifies registered plug-ins about state changes in a session object.
old-location: termserv\itssbresourcenotificationex_notifysessionchangeex.htm
tech.root: termserv
ms.assetid: 75f7371a-fd3e-4045-b8fe-23d57d75b27a
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ITsSbResourceNotificationEx interface [Remote Desktop Services],NotifySessionChangeEx method, ITsSbResourceNotificationEx.NotifySessionChangeEx, ITsSbResourceNotificationEx::NotifySessionChangeEx, NotifySessionChangeEx, NotifySessionChangeEx method [Remote Desktop Services], NotifySessionChangeEx method [Remote Desktop Services],ITsSbResourceNotificationEx interface, sbtsv/ITsSbResourceNotificationEx::NotifySessionChangeEx, termserv.itssbresourcenotificationex_notifysessionchangeex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
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
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourceNotificationEx.NotifySessionChangeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sbtsv.h
: 
- ITsSbResourceNotificationEx.NotifySessionChangeEx
: 
---

# ITsSbResourceNotificationEx::NotifySessionChangeEx


## -description


Notifies registered plug-ins about state changes in a session object.


## -parameters




### -param targetName [in]

The name of the target.


### -param userName [in]

The user name.


### -param domain [in]

The user domain.


### -param sessionId [in]

Identifies the session that changed.


### -param sessionState [in]

A <a href="https://msdn.microsoft.com/2780e704-72f1-44a9-ad54-ab3d2b19befe">TSSESSION_STATE</a> value specifying he type of change that occurred.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/70785b82-239d-4957-9703-ced685a2e0b8">ITsSbResourceNotification</a>



<a href="https://msdn.microsoft.com/5e40535d-62b2-4d16-a995-61c24aefb2e5">ITsSbResourceNotificationEx</a>
 

 


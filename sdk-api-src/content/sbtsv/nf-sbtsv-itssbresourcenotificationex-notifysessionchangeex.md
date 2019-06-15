---
UID: NF:sbtsv.ITsSbResourceNotificationEx.NotifySessionChangeEx
title: ITsSbResourceNotificationEx::NotifySessionChangeEx (sbtsv.h)
author: windows-sdk-content
description: Notifies registered plug-ins about state changes in a session object.
old-location: termserv\itssbresourcenotificationex_notifysessionchangeex.htm
tech.root: TermServ
ms.assetid: 75f7371a-fd3e-4045-b8fe-23d57d75b27a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotificationEx interface [Remote Desktop Services],NotifySessionChangeEx method, ITsSbResourceNotificationEx.NotifySessionChangeEx, ITsSbResourceNotificationEx::NotifySessionChangeEx, NotifySessionChangeEx, NotifySessionChangeEx method [Remote Desktop Services], NotifySessionChangeEx method [Remote Desktop Services],ITsSbResourceNotificationEx interface, sbtsv/ITsSbResourceNotificationEx::NotifySessionChangeEx, termserv.itssbresourcenotificationex_notifysessionchangeex
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
ms.custom: 19H1
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

A <a href="https://docs.microsoft.com/windows/desktop/api/sessdirpublictypes/ne-sessdirpublictypes-_tssession_state">TSSESSION_STATE</a> value specifying he type of change that occurred.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex">ITsSbResourceNotificationEx</a>
 

 


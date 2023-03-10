---
UID: NF:sbtsv.ITsSbResourceNotification.NotifySessionChange
title: ITsSbResourceNotification::NotifySessionChange (sbtsv.h)
description: Notifies registered plug-ins about state changes in a session object. (ITsSbResourceNotification.NotifySessionChange)
helpviewer_keywords: ["ITsSbResourceNotification interface [Remote Desktop Services]","NotifySessionChange method","ITsSbResourceNotification.NotifySessionChange","ITsSbResourceNotification::NotifySessionChange","NotifySessionChange","NotifySessionChange method [Remote Desktop Services]","NotifySessionChange method [Remote Desktop Services]","ITsSbResourceNotification interface","sbtsv/ITsSbResourceNotification::NotifySessionChange","termserv.itssbresourcenotification_notifysessionchange"]
old-location: termserv\itssbresourcenotification_notifysessionchange.htm
tech.root: TermServ
ms.assetid: c1efe806-a448-42d7-8bcd-bd763c00c732
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotification interface [Remote Desktop Services],NotifySessionChange method, ITsSbResourceNotification.NotifySessionChange, ITsSbResourceNotification::NotifySessionChange, NotifySessionChange, NotifySessionChange method [Remote Desktop Services], NotifySessionChange method [Remote Desktop Services],ITsSbResourceNotification interface, sbtsv/ITsSbResourceNotification::NotifySessionChange, termserv.itssbresourcenotification_notifysessionchange
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbResourceNotification::NotifySessionChange
 - sbtsv/ITsSbResourceNotification::NotifySessionChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourceNotification.NotifySessionChange
---

# ITsSbResourceNotification::NotifySessionChange


## -description

Notifies registered plug-ins about state changes in a session object.

## -parameters

### -param changeType [in]

The type of change that occurred.

### -param pSession [in]

A pointer to a session object. This object is a copy of the object present in the RD Connection Broker store. Any changes to this object do not affect the object in the store.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

RD Connection Broker calls the <b>NotifySessionChange</b> method to notify registered plug-ins about state changes in a session object. For example, RD Connection Broker calls this method when a new session is added to the resource plug-in store as a result of a session logon.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>

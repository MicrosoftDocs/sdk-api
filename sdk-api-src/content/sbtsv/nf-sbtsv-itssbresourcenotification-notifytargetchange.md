---
UID: NF:sbtsv.ITsSbResourceNotification.NotifyTargetChange
title: ITsSbResourceNotification::NotifyTargetChange (sbtsv.h)
description: Notifies registered plug-ins about state changes in a target object. (ITsSbResourceNotification.NotifyTargetChange)
helpviewer_keywords: ["ITsSbResourceNotification interface [Remote Desktop Services]","NotifyTargetChange method","ITsSbResourceNotification.NotifyTargetChange","ITsSbResourceNotification::NotifyTargetChange","NotifyTargetChange","NotifyTargetChange method [Remote Desktop Services]","NotifyTargetChange method [Remote Desktop Services]","ITsSbResourceNotification interface","sbtsv/ITsSbResourceNotification::NotifyTargetChange","termserv.itssbresourcenotification_notifytargetchange"]
old-location: termserv\itssbresourcenotification_notifytargetchange.htm
tech.root: TermServ
ms.assetid: d075c7ae-fe86-4547-a980-2b82ea3498c6
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotification interface [Remote Desktop Services],NotifyTargetChange method, ITsSbResourceNotification.NotifyTargetChange, ITsSbResourceNotification::NotifyTargetChange, NotifyTargetChange, NotifyTargetChange method [Remote Desktop Services], NotifyTargetChange method [Remote Desktop Services],ITsSbResourceNotification interface, sbtsv/ITsSbResourceNotification::NotifyTargetChange, termserv.itssbresourcenotification_notifytargetchange
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
 - ITsSbResourceNotification::NotifyTargetChange
 - sbtsv/ITsSbResourceNotification::NotifyTargetChange
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
 - ITsSbResourceNotification.NotifyTargetChange
---

# ITsSbResourceNotification::NotifyTargetChange


## -description

Notifies registered plug-ins about state changes in a target object.

## -parameters

### -param TargetChangeType [in]

A value of the <a href="/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-target_change_type">TARGET_CHANGE_TYPE</a> enumeration that specifies the type of change that occurred in a target.

### -param pTarget [in]

A pointer to a target object. This object is a copy of the object present in the RD Connection Broker store. Any changes to this object do not affect the object in the store.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

RD Connection Broker calls the <b>NotifyTargetChange</b> method to notify registered plug-ins about state changes in a target object. For example, RD Connection Broker calls this method when a new session is added to the resource plug-in store as a result of a session logon.

## -see-also

<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>



<a href="/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget">ITsSbTarget</a>



<a href="/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-target_change_type">TARGET_CHANGE_TYPE</a>

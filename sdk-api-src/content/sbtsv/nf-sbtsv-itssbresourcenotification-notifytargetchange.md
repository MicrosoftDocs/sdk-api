---
UID: NF:sbtsv.ITsSbResourceNotification.NotifyTargetChange
title: ITsSbResourceNotification::NotifyTargetChange
author: windows-sdk-content
description: Notifies registered plug-ins about state changes in a target object.
old-location: termserv\itssbresourcenotification_notifytargetchange.htm
old-project: termserv
ms.assetid: d075c7ae-fe86-4547-a980-2b82ea3498c6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITsSbResourceNotification interface [Remote Desktop Services],NotifyTargetChange method, ITsSbResourceNotification.NotifyTargetChange, ITsSbResourceNotification::NotifyTargetChange, NotifyTargetChange, NotifyTargetChange method [Remote Desktop Services], NotifyTargetChange method [Remote Desktop Services],ITsSbResourceNotification interface, sbtsv/ITsSbResourceNotification::NotifyTargetChange, termserv.itssbresourcenotification_notifytargetchange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourceNotification.NotifyTargetChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbResourceNotification::NotifyTargetChange


## -description


Notifies registered plug-ins about state changes in a target object.


## -parameters




### -param TargetChangeType [in]

A value of the <a href="https://msdn.microsoft.com/ee1e6433-498f-4d8a-97d7-3e32f79fafda">TARGET_CHANGE_TYPE</a> enumeration that specifies the type of change that occurred in a target.


### -param pTarget [in]

A pointer to a target object. This object is a copy of the object present in the RD Connection Broker store. Any changes to this object do not affect the object in the store.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



RD Connection Broker calls the <b>NotifyTargetChange</b> method to notify registered plug-ins about state changes in a target object. For example, RD Connection Broker calls this method when a new session is added to the resource plug-in store as a result of a session logon.




## -see-also




<a href="https://msdn.microsoft.com/70785b82-239d-4957-9703-ced685a2e0b8">ITsSbResourceNotification</a>



<a href="https://msdn.microsoft.com/bcb26b43-ec6e-4cc8-9d40-15a7a3a62582">ITsSbTarget</a>



<a href="https://msdn.microsoft.com/ee1e6433-498f-4d8a-97d7-3e32f79fafda">TARGET_CHANGE_TYPE</a>
 

 


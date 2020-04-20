---
UID: NF:sbtsv.ITsSbResourceNotificationEx.NotifyTargetChangeEx
title: ITsSbResourceNotificationEx::NotifyTargetChangeEx (sbtsv.h)
description: Notifies registered plug-ins about state changes in a target object.helpviewer_keywords: ["ITsSbResourceNotificationEx interface [Remote Desktop Services]","NotifyTargetChangeEx method","ITsSbResourceNotificationEx.NotifyTargetChangeEx","ITsSbResourceNotificationEx::NotifyTargetChangeEx","NotifyTargetChangeEx","NotifyTargetChangeEx method [Remote Desktop Services]","NotifyTargetChangeEx method [Remote Desktop Services]","ITsSbResourceNotificationEx interface","sbtsv/ITsSbResourceNotificationEx::NotifyTargetChangeEx","termserv.itssbresourcenotificationex_notifytargetchangeex"]
old-location: termserv\itssbresourcenotificationex_notifytargetchangeex.htm
tech.root: TermServ
ms.assetid: 8f1f07ce-4b5d-4e21-834d-f554bd73cc63
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotificationEx interface [Remote Desktop Services],NotifyTargetChangeEx method, ITsSbResourceNotificationEx.NotifyTargetChangeEx, ITsSbResourceNotificationEx::NotifyTargetChangeEx, NotifyTargetChangeEx, NotifyTargetChangeEx method [Remote Desktop Services], NotifyTargetChangeEx method [Remote Desktop Services],ITsSbResourceNotificationEx interface, sbtsv/ITsSbResourceNotificationEx::NotifyTargetChangeEx, termserv.itssbresourcenotificationex_notifytargetchangeex
f1_keywords:
- sbtsv/ITsSbResourceNotificationEx.NotifyTargetChangeEx
dev_langs:
- c++
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
- ITsSbResourceNotificationEx.NotifyTargetChangeEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITsSbResourceNotificationEx::NotifyTargetChangeEx


## -description


Notifies registered plug-ins about state changes in a target object.


## -parameters




### -param targetName [in]

The name of the target.


### -param targetChangeType [in]

A value of the <a href="https://docs.microsoft.com/windows/win32/api/sessdirpublictypes/ne-sessdirpublictypes-target_change_type">TARGET_CHANGE_TYPE</a> enumeration that specifies the type of change that occurred in a target.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification">ITsSbResourceNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex">ITsSbResourceNotificationEx</a>
 

 


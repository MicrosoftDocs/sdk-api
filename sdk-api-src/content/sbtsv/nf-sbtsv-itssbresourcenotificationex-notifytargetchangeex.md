---
UID: NF:sbtsv.ITsSbResourceNotificationEx.NotifyTargetChangeEx
title: ITsSbResourceNotificationEx::NotifyTargetChangeEx (sbtsv.h)
author: windows-sdk-content
description: Notifies registered plug-ins about state changes in a target object.
old-location: termserv\itssbresourcenotificationex_notifytargetchangeex.htm
tech.root: TermServ
ms.assetid: 8f1f07ce-4b5d-4e21-834d-f554bd73cc63
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITsSbResourceNotificationEx interface [Remote Desktop Services],NotifyTargetChangeEx method, ITsSbResourceNotificationEx.NotifyTargetChangeEx, ITsSbResourceNotificationEx::NotifyTargetChangeEx, NotifyTargetChangeEx, NotifyTargetChangeEx method [Remote Desktop Services], NotifyTargetChangeEx method [Remote Desktop Services],ITsSbResourceNotificationEx interface, sbtsv/ITsSbResourceNotificationEx::NotifyTargetChangeEx, termserv.itssbresourcenotificationex_notifytargetchangeex
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
 - ITsSbResourceNotificationEx.NotifyTargetChangeEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbResourceNotificationEx::NotifyTargetChangeEx


## -description


Notifies registered plug-ins about state changes in a target object.


## -parameters




### -param targetName [in]

The name of the target.


### -param targetChangeType [in]

A value of the <a href="https://msdn.microsoft.com/en-us/library/Ee351745(v=VS.85).aspx">TARGET_CHANGE_TYPE</a> enumeration that specifies the type of change that occurred in a target.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/70785b82-239d-4957-9703-ced685a2e0b8">ITsSbResourceNotification</a>



<a href="https://msdn.microsoft.com/5e40535d-62b2-4d16-a995-61c24aefb2e5">ITsSbResourceNotificationEx</a>
 

 


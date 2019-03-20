---
UID: NF:syncmgr.ISyncMgrEvent.GetLevel
title: ISyncMgrEvent::GetLevel (syncmgr.h)
author: windows-sdk-content
description: Gets the log level of the event.
old-location: shell\ISyncMgrEvent_GetLevel.htm
tech.root: shell
ms.assetid: 2937dc05-9576-43b4-9fbe-6c151dffcace
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetLevel, GetLevel method [Windows Shell], GetLevel method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetLevel method, ISyncMgrEvent.GetLevel, ISyncMgrEvent::GetLevel, _shell_ISyncMgrEvent_GetLevel, shell.ISyncMgrEvent_GetLevel, syncmgr/ISyncMgrEvent::GetLevel
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
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
 - Syncmgr.h
api_name:
 - ISyncMgrEvent.GetLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrEvent::GetLevel


## -description


Gets the log level of the event.


## -parameters




### -param pnLevel [out]

Type: <b><a href="https://msdn.microsoft.com/9a961cd2-c05f-47cf-a50a-40af18eac0cd">SYNCMGR_EVENT_LEVEL</a>*</b>

When this method returns, contains a pointer to a member of the <a href="https://msdn.microsoft.com/9a961cd2-c05f-47cf-a50a-40af18eac0cd">SYNCMGR_EVENT_LEVEL</a> enumeration that indicates the log level.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




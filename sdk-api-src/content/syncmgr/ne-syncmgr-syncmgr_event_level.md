---
UID: NE:syncmgr.SYNCMGR_EVENT_LEVEL
title: SYNCMGR_EVENT_LEVEL
author: windows-sdk-content
description: Specifies the type of event being reported to Sync Center.
old-location: shell\SYNCMGR_EVENT_LEVEL.htm
old-project: shell
ms.assetid: 9a961cd2-c05f-47cf-a50a-40af18eac0cd
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: SYNCMGR_EL_ERROR, SYNCMGR_EL_INFORMATION, SYNCMGR_EL_MAX, SYNCMGR_EL_WARNING, SYNCMGR_EVENT_LEVEL, SYNCMGR_EVENT_LEVEL enumeration [Windows Shell], shell.SYNCMGR_EVENT_LEVEL, shell_SYNCMGR_EVENT_LEVEL, syncmgr/SYNCMGR_EL_ERROR, syncmgr/SYNCMGR_EL_INFORMATION, syncmgr/SYNCMGR_EL_MAX, syncmgr/SYNCMGR_EL_WARNING, syncmgr/SYNCMGR_EVENT_LEVEL
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: SYNCMGR_EVENT_LEVEL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_EVENT_LEVEL
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# SYNCMGR_EVENT_LEVEL enumeration


## -description


Specifies the type of event being reported to Sync Center.


## -enum-fields




### -field SYNCMGR_EL_INFORMATION

The event is informational in nature and will be displayed with the appropriate icon.


### -field SYNCMGR_EL_WARNING

The event is a warning and will be displayed with the appropriate icon.


### -field SYNCMGR_EL_ERROR

The event is an error and will be displayed with the appropriate icon. Additionally, this event will be included in the count of errors reported to the handler or item when it is displayed in the folder as well as to the sync tray icon.


### -field SYNCMGR_EL_MAX

Used only to declare the largest valid value in this enumeration. Do not use with <a href="https://msdn.microsoft.com/4c7d6627-1652-4920-9dce-a61673e6e656">ISyncMgrSyncCallback::ReportEvent</a>.


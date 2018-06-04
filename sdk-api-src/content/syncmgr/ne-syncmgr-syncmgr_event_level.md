---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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


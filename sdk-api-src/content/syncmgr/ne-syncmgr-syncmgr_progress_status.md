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

# SYNCMGR_PROGRESS_STATUS enumeration


## -description


Specifies the current progress status of a synchronization process. Used by <a href="https://msdn.microsoft.com/fd7ed6f4-49c6-44c7-86f9-0b2c04d19de8">ISyncMgrSyncCallback::ReportProgress</a>.


## -enum-fields




### -field SYNCMGR_PS_UPDATING

The progress status is currently being updated by the handler.


### -field SYNCMGR_PS_UPDATING_INDETERMINATE

Ignore step parameters. The progress bar cycles from left to right on a timer internal to the sync folder. This is known as marquee mode.


### -field SYNCMGR_PS_SUCCEEDED

The synchronization is complete.


### -field SYNCMGR_PS_FAILED

Indicates something went wrong during the synchronization.


### -field SYNCMGR_PS_CANCELED

The user canceled the synchronization before it completed. Upon receipt of this value, Sync Center updates the UI and enables the option to restart the sync for that item.


### -field SYNCMGR_PS_DISCONNECTED

The device being synchronized was disconnected before the sync completed..


### -field SYNCMGR_PS_MAX

Used only to declare the largest valid value in this enumeration. Do not use with <a href="https://msdn.microsoft.com/fd7ed6f4-49c6-44c7-86f9-0b2c04d19de8">ISyncMgrSyncCallback::ReportProgress</a>.


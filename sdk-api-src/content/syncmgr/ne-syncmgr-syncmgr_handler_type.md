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

# SYNCMGR_HANDLER_TYPE enumeration


## -description


Specifies the type of a handler. Used by <a href="https://msdn.microsoft.com/466c5bd5-0166-4c0d-801d-a155f20140ce">ISyncMgrHandlerInfo::GetType</a>.


## -enum-fields




### -field SYNCMGR_HT_UNSPECIFIED

The handler type is unknown. This value is also used if <a href="https://msdn.microsoft.com/466c5bd5-0166-4c0d-801d-a155f20140ce">ISyncMgrHandlerInfo::GetType</a> fails.


### -field SYNCMGR_HT_APPLICATION

The handler is an application.


### -field SYNCMGR_HT_DEVICE

The handler syncs with a device such as a phone or PDA.


### -field SYNCMGR_HT_FOLDER

The handler syncs with local or remote folders.


### -field SYNCMGR_HT_SERVICE

The handler syncs with a web service.


### -field SYNCMGR_HT_COMPUTER

The handler syncs with a computer.


### -field SYNCMGR_HT_MIN

Indicates the minimum <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HANDLER_TYPE</a> value.


### -field SYNCMGR_HT_MAX

Indicates the maximum <a href="https://msdn.microsoft.com/993a1d55-32ee-4ea7-823f-a533e9646f1f">SYNCMGR_HANDLER_TYPE</a> value.


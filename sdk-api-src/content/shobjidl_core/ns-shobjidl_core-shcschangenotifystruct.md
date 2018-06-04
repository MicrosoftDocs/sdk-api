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

# SHCSCHANGENOTIFYSTRUCT structure


## -description


Contains information about change notification. It is used by <a href="https://msdn.microsoft.com/06809b61-041b-41bd-82dd-0d64edf8bbae">IShellMenuCallback::CallbackSM</a>.


## -struct-fields




### -field lEvent

Type: <b>long</b>

An SHCNE value that specifies the type of change that took place. See <a href="https://msdn.microsoft.com/a9222ce9-0d06-4fd0-af3a-fd0e979713ce">SHChangeNotify</a> for a complete list of these values.


### -field pidl1

Type: <b>PCIDLIST_ABSOLUTE</b>

PIDL provided by the change notification. The target of this PIDL varies depending on the value of <b>lEvent</b>.


### -field pidl2

Type: <b>PCIDLIST_ABSOLUTE</b>

A second PIDL provided by the change notification. Not all <b>lEvent</b> values make use of this parameter, in which case its value is <b>NULL</b>.


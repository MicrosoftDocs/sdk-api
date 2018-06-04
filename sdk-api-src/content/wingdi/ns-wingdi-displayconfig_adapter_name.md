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

# DISPLAYCONFIG_ADAPTER_NAME structure


## -description


The DISPLAYCONFIG_ADAPTER_NAME structure contains information about the display adapter.


## -struct-fields




### -field header

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff553920">DISPLAYCONFIG_DEVICE_INFO_HEADER</a> structure that contains information about the request for the adapter name. The caller should set the <b>type</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to DISPLAYCONFIG_DEVICE_INFO_GET_ADAPTER_NAME and the <b>adapterId</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to the adapter identifier of the adapter for which the caller wants the name. For this request, the caller does not need to set the <b>id</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER. The caller should set the <b>size</b> member of DISPLAYCONFIG_DEVICE_INFO_HEADER to at least the size of the DISPLAYCONFIG_ADAPTER_NAME structure.


### -field adapterDevicePath

A NULL-terminated WCHAR string that is the  device name for the adapter. This name can be used with <i>SetupAPI.dll</i> to obtain the device name that is contained in the installation package.


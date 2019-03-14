---
UID: NS:wsdtypes._WSD_HOST_METADATA
title: WSD_HOST_METADATA
author: windows-sdk-content
description: Provides metadata for all services hosted by a device.
old-location: ncd\wsd_host_metadata_struct.htm
tech.root: WsdApi
ms.assetid: da774582-3b27-470d-9b6a-ac2b106a47b9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WSD_HOST_METADATA, WSD_HOST_METADATA structure, ncd.wsd_host_metadata_struct, wsdtypes/WSD_HOST_METADATA
ms.topic: struct
req.header: wsdtypes.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - WsdTypes.h
api_name:
 - WSD_HOST_METADATA
product: Windows
targetos: Windows
req.typenames: WSD_HOST_METADATA
req.redist: 
---

# WSD_HOST_METADATA structure


## -description


Provides metadata for all services hosted by a device.




## -struct-fields




### -field Host

Reference to a <a href="https://msdn.microsoft.com/1f80e36f-06ca-41fc-bbd7-b44823c75d4d">WSD_SERVICE_METADATA</a> structure that describes the parent service or the device.


### -field Hosted

Reference to a <a href="https://msdn.microsoft.com/f5975443-00e3-44f0-9a69-02460d4312c5">WSD_SERVICE_METADATA_LIST</a> structure that represents the singly linked list of services hosted by the parent service.


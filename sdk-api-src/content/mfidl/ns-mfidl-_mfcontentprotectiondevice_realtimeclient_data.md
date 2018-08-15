---
UID: NS:mfidl._MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
title: "_MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA"
author: windows-sdk-content
description: Advises the secure processor of the Multimedia Class Scheduler service (MMCSS) parameters so that real-time tasks can be scheduled at the expected priority.
old-location: mf\mfcontentprotectiondevice_realtimeclient_data.htm
old-project: medfound
ms.assetid: E0A98B31-13D4-4281-AFFB-A3DA664CE876
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA, MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA structure [Media Foundation], _MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA, mf.mfcontentprotectiondevice_realtimeclient_data, mfidl/MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mfidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFCONTENTPROTECTIONDEVICE_REALTIMECLIENT_DATA structure


## -description


Advises the secure processor of the  Multimedia Class Scheduler service (MMCSS) parameters so that real-time tasks can be scheduled at the expected priority.


## -struct-fields




### -field TaskIndex

The identifier for the MMCSS task.


### -field ClassName

The name of the MMCSS task.


### -field BasePriority

The base priority of the thread that runs the MMCSS task.


## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 


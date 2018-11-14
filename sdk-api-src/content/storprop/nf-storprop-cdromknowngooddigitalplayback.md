---
UID: NF:storprop.CdromKnownGoodDigitalPlayback
title: CdromKnownGoodDigitalPlayback function
author: windows-sdk-content
description: Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.
old-location: base\cdromknowngooddigitalplayback.htm
tech.root: devio
ms.assetid: df242729-2082-4608-bd73-4c8d215a09ea
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: CdromKnownGoodDigitalPlayback, CdromKnownGoodDigitalPlayback function, base.cdromknowngooddigitalplayback, storprop/CdromKnownGoodDigitalPlayback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: storprop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.dll: Storprop.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Storprop.dll
api_name:
 - CdromKnownGoodDigitalPlayback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- CdromKnownGoodDigitalPlayback
: 
---

# CdromKnownGoodDigitalPlayback function


## -description


Determines whether the specified CD-ROM or DVD drive has digital playback that is known to be good.


## -parameters




### -param HDevInfo [in]

A handle to a device information set listing the devices for which information is to be returned. This handle is typically returned by the <b>SetupDiGetClassDevs</b> or <b>SetupDiGetClassDevsEx</b> function.


### -param DevInfoData [in]

A pointer to an <b>SP_DEVINFO_DATA</b> structure that defines the device instance.


## -returns



If digital playback is good, the return value is <b>TRUE</b>. Otherwise, the return value is <b>FALSE</b>.




## -remarks



This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Storprop.dll.




## -see-also




<a href="https://msdn.microsoft.com/3918ba49-1549-4f0c-b9fd-303ef46b810e">Device Management Functions</a>
 

 


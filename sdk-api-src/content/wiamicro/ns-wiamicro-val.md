---
UID: NS:wiamicro.VAL
title: VAL
author: windows-driver-content
description: The VAL structure is used by the microdriver and WIA Flatbed driver to pass information between each other.
old-location: image\val.htm
old-project: image
ms.assetid: 9c9cf520-3249-4c1e-9d0d-e07f7127117e
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: "*PVAL, MicroDrv_397b66fc-2f8e-434e-88ac-24b5cdd415d5.xml, PVAL, PVAL structure pointer [Imaging Devices], VAL, VAL structure [Imaging Devices], image.val, wiamicro/PVAL, wiamicro/VAL"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wiamicro.h
req.include-header: Wiamicro.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Me and in Windows XP and later versions of the Windows operating systems.
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
req.typenames: VAL, *PVAL
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	wiamicro.h
api_name:
-	VAL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# VAL structure


## -description


The VAL structure is used by the microdriver and WIA Flatbed driver to pass information between each other.


## -struct-fields




### -field lVal

Specifies a command value to return to the WIA Flatbed driver. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552714">WIA Microdriver Commands</a> for a list of available commands for this parameter.


### -field dblVal

Specifies a command value to return to the WIA Flatbed driver. See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552714">WIA Microdriver Commands</a> for a list of available commands for this parameter.


### -field pGuid

Points to the GUID of the pressed button. If no button was pressed, this member points to GUID_NULL.


### -field pScanInfo

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff547361">SCANINFO</a> structure.


### -field handle

Points to a ShutDown event handle that will be signaled by the WIA Flatbed Driver when the driver is being unloaded or shut down. 


### -field ppButtonNames

Specifies the address of a pointer to an array of button names.


### -field pHandle

Points to an event handle.


### -field lReserved

Reserved. Do not use.


### -field szVal

Specifies the device name in ASCII form. If needed for interrupt checking, the microdriver can use this name to pass to <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> (described in the Microsoft Windows SDK documentation) in order to obtain a file handle to the device.


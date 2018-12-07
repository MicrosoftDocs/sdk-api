---
UID: NS:dinputd.DIDRIVERVERSIONS
title: DIDRIVERVERSIONS
author: windows-sdk-content
description: The DIDRIVERVERSIONS structure is used by the DirectInput effect driver to report version information back to DirectInput.
old-location: hid\didriverversions.htm
tech.root: hid
ms.assetid: 28e24657-a75e-49d1-88b0-3e40ba8851ae
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDIDRIVERVERSIONS, DIDRIVERVERSIONS, DIDRIVERVERSIONS structure [Human Input Devices], di_ref_8a99e6d1-de51-4729-bcce-c201030bc557.xml, dinputd/DIDRIVERVERSIONS, hid.didriverversions"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dinputd.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dinputd.h
api_name:
 - DIDRIVERVERSIONS
product: Windows
targetos: Windows
req.typenames: DIDRIVERVERSIONS, *LPDIDRIVERVERSIONS
req.redist: 
---

# DIDRIVERVERSIONS structure


## -description


The <b>DIDRIVERVERSIONS</b> structure is used by the DirectInput effect driver to report version information back to DirectInput. The semantics of the version numbers are left to the discretion of the device driver. The only requirement is that later versions have higher version numbers than earlier versions. 


## -struct-fields




### -field dwSize

Specifies the size of the structure in bytes. This member must be initialized before the structure is used. 


### -field dwFirmwareRevision

Specifies the firmware revision of the device. 


### -field dwHardwareRevision

Specifies the hardware revision of the device. 


### -field dwFFDriverVersion

Specifies the version number of the force-feedback device driver. 


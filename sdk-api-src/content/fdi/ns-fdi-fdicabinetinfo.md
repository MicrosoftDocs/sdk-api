---
UID: NS:fdi.FDICABINETINFO
title: FDICABINETINFO
author: windows-sdk-content
description: The FDICABINETINFO structure contains details about a particular cabinet file.
old-location: winprog\fdicabinetinfo.htm
tech.root: DevNotes
ms.assetid: fde1a2ca-60cd-4a4d-9872-681e2f8f4fb1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PFDICABINETINFO, FDICABINETINFO, FDICABINETINFO FAR *PFDICABINETINFO, FDICABINETINFO FAR *PFDICABINETINFO structure [Windows API], FDICABINETINFO structure [Windows API], fdi/FDICABINETINFO, winprog.fdicabinetinfo"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: fdi.h
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
 - Fdi.h
api_name:
 - FDICABINETINFO FAR *PFDICABINETINFO
product: Windows
targetos: Windows
req.typenames: FDICABINETINFO
req.redist: 
---

# FDICABINETINFO structure


## -description


The <b>FDICABINETINFO</b> structure contains details about a particular cabinet file.


## -struct-fields




### -field cbCabinet

The total length of the cabinet file.


### -field cFolders

The count of the folders in the cabinet.


### -field cFiles

The count of the files in the cabinet.


### -field setID

The identifier of the cabinet set.


### -field iCabinet

The cabinet number in set. This index is zero based.


### -field fReserve

If this value is set to <b>TRUE</b>, a reserved area is present in the cabinet.


### -field hasprev

If this value is set to <b>TRUE</b>, the cabinet is linked to a previous cabinet. This is accomplished by having a file continued from the previous cabinet into the current one.


### -field hasnext

If this value is set to <b>TRUE</b>, the current cabinet is linked to the next cabinet by having a file continued from the current cabinet into the next one.


## -see-also




<a href="https://msdn.microsoft.com/01d223ca-56c6-49fa-b9e6-e5eeda88936a">FDIIsCabinet</a>
 

 


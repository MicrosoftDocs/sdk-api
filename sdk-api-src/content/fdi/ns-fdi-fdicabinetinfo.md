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
 

 


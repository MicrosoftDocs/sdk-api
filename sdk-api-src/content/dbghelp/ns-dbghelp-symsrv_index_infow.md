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

# SYMSRV_INDEX_INFOW structure


## -description


Contains symbol server index information.


## -struct-fields




### -field sizeofstruct

The size of the structure, in bytes. This member must be set to <code>sizeof(SYMSRV_INDEX_INFO)</code> or <code>sizeof(SYMSRV_INDEX_INFOW)</code>.


### -field file

The name of the .pdb, .dbg, or image file.


### -field stripped

A value that indicates whether the image file is stripped.


### -field timestamp

The timestamp from the PE header. This member is used only for image files.


### -field size

The file size from the PE header. This member is used only for image files.


### -field dbgfile

If the image file is stripped and there is a .dbg file, this member is the path to the .dbg file from the CV record.


### -field pdbfile

The .pdb file from the CV record. This member is used only for image and .dbg files.


### -field guid

The GUID of the .pdb file. If there is no GUID available, the signature of the .pdb file is copied into first <b>DWORD</b> of the GUID.


### -field sig

The signature of the .pdb file (for use with old-style .pdb files). This value can be 0 if it is a new-style .pdb file that uses a GUID-length signature.


### -field age

The age of the .pdb file.


## -see-also




<a href="https://msdn.microsoft.com/ee5b0821-2746-467e-9d95-90776882ac95">SymSrvGetFileIndexInfo</a>
 

 


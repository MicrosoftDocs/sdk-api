---
UID: NS:dbghelp.SYMSRV_INDEX_INFO
title: SYMSRV_INDEX_INFO
author: windows-sdk-content
description: Contains symbol server index information.
old-location: base\symsrv_index_info.htm
old-project: Debug
ms.assetid: 110cf21c-7768-48fd-bfdc-1f7cd30ca291
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: "*PSYMSRV_INDEX_INFO, PSYMSRV_INDEX_INFO, PSYMSRV_INDEX_INFO structure pointer, SYMSRV_INDEX_INFO, SYMSRV_INDEX_INFO structure, SYMSRV_INDEX_INFOW, base.symsrv_index_info, dbghelp/PSYMSRV_INDEX_INFO, dbghelp/SYMSRV_INDEX_INFO, dbghelp/SYMSRV_INDEX_INFOW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SYMSRV_INDEX_INFOW (Unicode) and SYMSRV_INDEX_INFO (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SYMSRV_INDEX_INFO, *PSYMSRV_INDEX_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Dbghelp.h
api_name:
-	SYMSRV_INDEX_INFO
-	SYMSRV_INDEX_INFO
-	SYMSRV_INDEX_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# SYMSRV_INDEX_INFO structure


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
 

 


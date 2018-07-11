---
UID: NS:winbase._OFSTRUCT
title: "_OFSTRUCT"
author: windows-sdk-content
description: Contains information about a file that the OpenFile function opened or attempted to open.
old-location: fs\ofstruct_str.htm
old-project: fileio
ms.assetid: 195581e5-e962-4756-a33c-b1e898b5b0e7
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: "*LPOFSTRUCT, *POFSTRUCT, OFSTRUCT, OFSTRUCT structure [Files], POFSTRUCT, POFSTRUCT structure pointer [Files], _OFSTRUCT, _win32_ofstruct_str, base.ofstruct_str, fs.ofstruct_str, winbase/OFSTRUCT, winbase/POFSTRUCT"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: OFSTRUCT, *LPOFSTRUCT, *POFSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinBase.h
api_name:
 - OFSTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _OFSTRUCT structure


## -description


Contains information about a file that the 
<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a> function opened or attempted to open.


## -struct-fields




### -field cBytes

The size of the structure, in bytes.


### -field fFixedDisk

If this member is nonzero, the file is on a hard (fixed) disk. Otherwise, it is not.


### -field nErrCode

The MS-DOS error code if the 
<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a> function failed.


### -field Reserved1

Reserved; do not use.


### -field Reserved2

Reserved; do not use.


### -field szPathName

The path and file name of the file.


## -see-also




<a href="https://msdn.microsoft.com/800f4d40-252a-44fe-b10d-348c22d69355">OpenFile</a>
 

 


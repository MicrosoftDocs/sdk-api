---
UID: NC:vdmdbg.PROCESSENUMPROC
title: PROCESSENUMPROC (vdmdbg.h)
description: Implement this function to receive information for each virtual DOS machine (VDM) that VDMEnumProcessWOW enumerates.
helpviewer_keywords: ["PROCESSENUMPROC","PROCESSENUMPROC callback","PROCESSENUMPROC callback function [Windows API]","vdmdbg/PROCESSENUMPROC","winprog.processvdms"]
old-location: winprog\processvdms.htm
tech.root: winprog
ms.assetid: ba5ce19d-4f37-4764-9a76-0f1013f9ea0f
ms.date: 12/05/2018
ms.keywords: PROCESSENUMPROC, PROCESSENUMPROC callback, PROCESSENUMPROC callback function [Windows API], vdmdbg/PROCESSENUMPROC, winprog.processvdms
req.header: vdmdbg.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PROCESSENUMPROC
 - vdmdbg/PROCESSENUMPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - VdmDbg.h
api_name:
 - PROCESSENUMPROC
---

# PROCESSENUMPROC callback function


## -description

<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future.]

Implement this function to receive information for each virtual DOS machine (VDM) that <a href="/windows/desktop/api/vdmdbg/nf-vdmdbg-vdmenumprocesswow">VDMEnumProcessWOW</a> enumerates. 
			

The <b>PROCESSENUMPROC</b> type defines a pointer to this callback function. <b>ProcessVDMs</b> is a placeholder for the application-defined function name.

## -parameters

### -param dwProcessId [out]

The process ID of the NTVDM.exe process. Use this ID when calling other VDM debug functions.

### -param dwAttributes [out]

The process attributes.

### -param lpUserDefined [out]

The user-defined data that was passed to the <a href="/windows/desktop/api/vdmdbg/nf-vdmdbg-vdmenumprocesswow">VDMEnumProcessWOW</a> function.

## -returns

Return <b>TRUE</b> to stop the enumeration and <b>FALSE</b> to continue.
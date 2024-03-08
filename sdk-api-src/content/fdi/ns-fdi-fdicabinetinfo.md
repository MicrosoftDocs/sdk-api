---
UID: NS:fdi.FDICABINETINFO
title: FDICABINETINFO (fdi.h)
description: The FDICABINETINFO structure contains details about a particular cabinet file.
helpviewer_keywords: ["*PFDICABINETINFO","FDICABINETINFO","FDICABINETINFO FAR *PFDICABINETINFO","FDICABINETINFO FAR *PFDICABINETINFO structure [Windows API]","FDICABINETINFO structure [Windows API]","fdi/FDICABINETINFO","winprog.fdicabinetinfo"]
old-location: winprog\fdicabinetinfo.htm
tech.root: winprog
ms.assetid: fde1a2ca-60cd-4a4d-9872-681e2f8f4fb1
ms.date: 12/05/2018
ms.keywords: '*PFDICABINETINFO, FDICABINETINFO, FDICABINETINFO FAR *PFDICABINETINFO, FDICABINETINFO FAR *PFDICABINETINFO structure [Windows API], FDICABINETINFO structure [Windows API], fdi/FDICABINETINFO, winprog.fdicabinetinfo'
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
targetos: Windows
req.typenames: FDICABINETINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FDICABINETINFO
 - fdi/FDICABINETINFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fdi.h
api_name:
 - FDICABINETINFO FAR *PFDICABINETINFO
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

<a href="/windows/desktop/api/fdi/nf-fdi-fdiiscabinet">FDIIsCabinet</a>


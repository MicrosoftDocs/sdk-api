---
UID: NS:fci.CCAB
title: CCAB (fci.h)
description: The CCAB structure contains cabinet information.
helpviewer_keywords: ["*PCCAB","CCAB","CCAB structure [Windows API]","PCCAB","PCCAB structure pointer [Windows API]","fci/CCAB","fci/PCCAB","winprog.ccab"]
old-location: winprog\ccab.htm
tech.root: winprog
ms.assetid: e25cb72b-4c96-40e9-9fd5-2920e4a01d3a
ms.date: 12/05/2018
ms.keywords: '*PCCAB, CCAB, CCAB structure [Windows API], PCCAB, PCCAB structure pointer [Windows API], fci/CCAB, fci/PCCAB, winprog.ccab'
req.header: fci.h
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
req.typenames: CCAB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CCAB
 - fci/CCAB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fci.h
api_name:
 - CCAB
---

## -description

The <b>CCAB</b> structure contains cabinet information.

## -struct-fields

### -field cb

The maximum size, in bytes, of a cabinet  created by FCI.

### -field cbFolderThresh

The maximum size, in bytes, that  a folder will contain before a new folder is created.

### -field cbReserveCFHeader

The size, in bytes, of the CFHeader reserve area. Possible value range is 0-60,000.

### -field cbReserveCFFolder

The size, in bytes, of the CFFolder reserve area. Possible value range is 0-255.

### -field cbReserveCFData

The size, in bytes, of the CFData reserve area. Possible value range is 0-255.

### -field iCab

The number of created cabinets.

### -field iDisk

The maximum size, in bytes, of a cabinet  created by FCI.

### -field fFailOnIncompressible

TBD

### -field setID

A value that represents the association between a collection of linked cabinet files.

### -field szDisk

The name of the disk on which the cabinet is placed.

### -field szCab

The name of the cabinet.

### -field szCabPath

The full path that indicates where to create the cabinet.

## -see-also

<a href="/windows/desktop/api/fci/nf-fci-fcicreate">FCICreate</a>


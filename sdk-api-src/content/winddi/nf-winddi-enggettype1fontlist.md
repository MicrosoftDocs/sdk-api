---
UID: NF:winddi.EngGetType1FontList
title: EngGetType1FontList function (winddi.h)
description: The EngGetType1FontList function retrieves a list of PostScript Type 1 fonts that are installed both locally and remotely.
helpviewer_keywords: ["EngGetType1FontList","EngGetType1FontList function [Display Devices]","display.enggettype1fontlist","gdifncs_66e06beb-5f9a-4184-9ab8-a0aca467e59d.xml","winddi/EngGetType1FontList"]
old-location: display\enggettype1fontlist.htm
tech.root: display
ms.assetid: 66f8ca3d-2080-4560-8e64-1dc26ceaaad4
ms.date: 12/05/2018
ms.keywords: EngGetType1FontList, EngGetType1FontList function [Display Devices], display.enggettype1fontlist, gdifncs_66e06beb-5f9a-4184-9ab8-a0aca467e59d.xml, winddi/EngGetType1FontList
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngGetType1FontList
 - winddi/EngGetType1FontList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-full-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngGetType1FontList
---

# EngGetType1FontList function


## -description

The <b>EngGetType1FontList</b> function retrieves a list of PostScript Type 1 fonts that are installed both locally and remotely.

## -parameters

### -param hdev [in]

Handle to the device. This is the GDI handle received by the driver as the <i>hdev</i> parameter for <a href="/windows/desktop/api/winddi/nf-winddi-drvcompletepdev">DrvCompletePDEV</a>.

### -param pType1Buffer [out, optional]

Pointer to an array of <a href="/windows/desktop/api/winddi/ns-winddi-type1_font">TYPE1_FONT</a> structures in which to store the Type 1 font list. This parameter can be <b>NULL</b>.

### -param cjType1Buffer [in]

Specifies the size, in bytes, of <i>pType1Buffer</i>.

### -param pulLocalFonts [out]

Pointer to a memory location that receives the number of Type 1 fonts on the local system.

### -param pulRemoteFonts [out]

Pointer to a memory location that receives the number of Type 1 fonts on the remote system.

### -param pLastModified [out]

Pointer to a memory location that receives the time stamp corresponding to the last time a Type 1 font was added or removed from the local system.

## -returns

<b>EngGetType1FontList</b> returns <b>TRUE</b> if it succeeds; otherwise, it returns <b>FALSE</b>.

## -remarks

PostScript printer drivers can call <b>EngGetType1FontList</b> to obtain a list of Type 1 fonts available to them. These fonts can then be accessed through the handles returned in the TYPE1_FONT structure.

If <i>pType1Buffer</i> is <b>NULL</b>, <b>EngGetType1FontList</b> returns only the number of local and remote Type 1 fonts, as well as the time stamp corresponding to the last time a Type 1 font was added or removed locally from the system.

## -see-also

<a href="/windows/desktop/api/winddi/ns-winddi-type1_font">TYPE1_FONT</a>
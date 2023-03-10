---
UID: NS:mmc._SMMCObjectTypes
title: SMMCObjectTypes (mmc.h)
description: The SMMCDynamicExtensions structure is introduced in MMC 1.1.
helpviewer_keywords: ["SMMCDynamicExtensions","SMMCDynamicExtensions structure [MMC]","SMMCObjectTypes","SMMCObjectTypes structure [MMC]","_slate_smmcdynamicextensions","mmc.smmcdynamicextensions","mmc/SMMCDynamicExtensions"]
old-location: mmc\smmcdynamicextensions.htm
tech.root: mmc
ms.assetid: 59acd90c-60de-457a-94d7-418b79247a2e
ms.date: 12/05/2018
ms.keywords: SMMCDynamicExtensions, SMMCDynamicExtensions structure [MMC], SMMCObjectTypes, SMMCObjectTypes structure [MMC], _slate_smmcdynamicextensions, mmc.smmcdynamicextensions, mmc/SMMCDynamicExtensions
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: SMMCObjectTypes
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SMMCObjectTypes
 - mmc/_SMMCObjectTypes
 - SMMCObjectTypes
 - mmc/SMMCObjectTypes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SMMCObjectTypes
---

# SMMCObjectTypes structure


## -description

The 
<b>SMMCDynamicExtensions</b> structure is introduced in MMC 1.1.

The 
<b>SMMCDynamicExtensions</b> structure defines the format of the data for the 
<a href="/previous-versions/windows/desktop/mmc/ccf-mmc-dynamic-extensions">CCF_MMC_DYNAMIC_EXTENSIONS</a> clipboard format, which specifies the non-namespace extension snap-ins that should extend a scope or result item.

## -struct-fields

### -field count

The count of GUIDs in the array specified by <b>guid</b>.

### -field guid

An array of GUIDs that represent the CLSIDs of the snap-ins that you want to extend the item represented by an <b>IDataObject</b> object.

## -remarks

For a snap-in to support dynamic extension of its items with non-namespace extensions (that is, context menu, toolbar, property sheet, or taskpad extensions), the clipboard format CCF_MMC_DYNAMIC_EXTENSIONS must be handled in the snap-in's <b>IDataObject</b> implementation. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/dynamic-non-namespace-extensions">Dynamic Non-Namespace Extensions</a>.

Be aware that the extension snap-in must be a non-namespace extension and the MMC registry entries for the snap-in to be extended as well as the extension snap-in must be set correctly. For details on setting MMC registry entries for extensions, see 
<a href="/previous-versions/windows/desktop/mmc/registration-requirements-for-extension-snap-ins">Registration Requirements for Extension Snap-ins</a>.

The CCF_MMC_DYNAMIC_EXTENSIONS clipboard format extends only non-namespace extensions. To dynamically add namespace extensions, the snap-in must use the 
<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-addextension">IConsoleNameSpace2::AddExtension</a> method. For more information, see 
<a href="/previous-versions/windows/desktop/mmc/dynamic-namespace-extensions">Dynamic Namespace Extensions</a>.

Just before MMC must use an extensible feature (that is, just before creating and that displays a context menu, property sheet, toolbar, or taskpad), MMC calls <b>IDataObject::GetDataHere</b> on the data object for the selected item and asks for dynamic extensions to add through the CCF_MMC_DYNAMIC_EXTENSIONS clipboard format. Based on CLSIDs passed in the 
<b>SMMCDynamicExtensions</b> structure, MMC attempts to add the specified extensions to the extensible feature. If an extension is unavailable or unregistered, MMC skips that extension and continues to the next CLSID passed in the structure.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-mmc-dynamic-extensions">CCF_MMC_DYNAMIC_EXTENSIONS</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iconsolenamespace2-addextension">IConsoleNameSpace2::AddExtension</a>



<a href="/windows/desktop/api/mmc/ns-mmc-smmcobjecttypes">SMMCObjectTypes</a>
---
UID: NS:mmc._MMC_EXT_VIEW_DATA
title: MMC_EXT_VIEW_DATA (mmc.h)
description: The MMC_EXT_VIEW_DATA structure is introduced in MMC 2.0.
helpviewer_keywords: ["*PMMC_EXT_VIEW_DATA","MMC_EXT_VIEW_DATA","MMC_EXT_VIEW_DATA structure [MMC]","PMMC_EXT_VIEW_DATA","PMMC_EXT_VIEW_DATA structure pointer [MMC]","_slate_mmc_ext_view_data","mmc.mmc_ext_view_data","mmc/MMC_EXT_VIEW_DATA","mmc/PMMC_EXT_VIEW_DATA"]
old-location: mmc\mmc_ext_view_data.htm
tech.root: mmc
ms.assetid: 8396e786-a0ea-4ff8-b899-a23e6552aa92
ms.date: 12/05/2018
ms.keywords: '*PMMC_EXT_VIEW_DATA, MMC_EXT_VIEW_DATA, MMC_EXT_VIEW_DATA structure [MMC], PMMC_EXT_VIEW_DATA, PMMC_EXT_VIEW_DATA structure pointer [MMC], _slate_mmc_ext_view_data, mmc.mmc_ext_view_data, mmc/MMC_EXT_VIEW_DATA, mmc/PMMC_EXT_VIEW_DATA'
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
req.typenames: MMC_EXT_VIEW_DATA, *PMMC_EXT_VIEW_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_EXT_VIEW_DATA
 - mmc/_MMC_EXT_VIEW_DATA
 - PMMC_EXT_VIEW_DATA
 - mmc/PMMC_EXT_VIEW_DATA
 - MMC_EXT_VIEW_DATA
 - mmc/MMC_EXT_VIEW_DATA
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
 - MMC_EXT_VIEW_DATA
---

# MMC_EXT_VIEW_DATA structure


## -description

The 
<b>MMC_EXT_VIEW_DATA</b> structure is introduced in MMC 2.0.

The 
<b>MMC_EXT_VIEW_DATA</b> structure is used by a view extension when it adds a view to the result pane.

## -struct-fields

### -field viewID

GUID for the view; this value uniquely identifies the view and is used to restore the view.

### -field pszURL

URL to the HTML used in the result pane; this typically points to an HTML resource in the snap-in's DLL.

### -field pszViewTitle

Title of the view extension.

### -field pszTooltipText

This value is reserved for future use.

### -field bReplacesDefaultView

If <b>TRUE</b>, the <b>Standard</b> tab does not appear in the tab selector; otherwise, the <b>Standard</b> tab appears. There is usually no need to display the <b>Standard</b> tab if the view extension snap-in displays the list of the primary snap-in.

## -remarks

For an example of the 
<b>MMC_EXT_VIEW_DATA</b> structure used in C++ code, see 
<a href="/windows/desktop/api/mmc/nf-mmc-iviewextensioncallback-addview">IViewExtensionCallback::AddView</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/extending-views">Extending Views</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iviewextensioncallback">IViewExtensionCallback</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iviewextensioncallback-addview">IViewExtensionCallback::AddView</a>



<a href="/previous-versions/windows/desktop/mmc/view-extension-mechanism">View Extension Mechanism</a>
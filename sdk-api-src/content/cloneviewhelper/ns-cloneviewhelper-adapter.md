---
UID: NS:cloneviewhelper.tagAdapter
title: Adapter (cloneviewhelper.h)
description: The Adapter structure describes a graphics adapter.
helpviewer_keywords: ["Adapter","Adapter structure [Display Devices]","TMM_Ref_6570c45d-9024-46c4-bcd4-848eb2d18955.xml","cloneviewhelper/Adapter","display.adapter"]
old-location: display\adapter.htm
tech.root: display
ms.assetid: c62c6aed-2593-4b5d-884f-99d20e269eb1
ms.date: 12/05/2018
ms.keywords: Adapter, Adapter structure [Display Devices], TMM_Ref_6570c45d-9024-46c4-bcd4-848eb2d18955.xml, cloneviewhelper/Adapter, display.adapter
req.header: cloneviewhelper.h
req.include-header: Cloneviewhelper.h
req.target-type: Windows
req.target-min-winverclnt: Available in Windows Vista and later versions of the Windows operating systems.
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
req.typenames: Adapter
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAdapter
 - cloneviewhelper/tagAdapter
 - Adapter
 - cloneviewhelper/Adapter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - cloneviewhelper.h
api_name:
 - Adapter
---

# Adapter structure


## -description

The Adapter structure describes a graphics adapter.

## -struct-fields

### -field AdapterName

A single wide-character string that holds the name of the graphics adapter.

### -field numSources

The number of video present sources in the array that the <b>sources</b> member specifies.

### -field sources

An array of <a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-sources">Sources</a> structures that specify a list of Video Present Network (VidPN) topologies.

## -see-also

<a href="/previous-versions/windows/hardware/drivers/ff568176(v=vs.85)">IViewHelper::SetConfiguration</a>



<a href="/windows/desktop/api/cloneviewhelper/ns-cloneviewhelper-sources">Sources</a>
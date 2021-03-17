---
UID: NS:mmc._MMC_EXPANDSYNC_STRUCT
title: MMC_EXPANDSYNC_STRUCT (mmc.h)
description: The MMC_EXPANDSYNC_STRUCT structure is introduced in MMC 1.1.
helpviewer_keywords: ["MMC_EXPANDSYNC_STRUCT","MMC_EXPANDSYNC_STRUCT structure [MMC]","_slate_mmc_expandsync_struct","mmc.mmc_expandsync_struct","mmc/MMC_EXPANDSYNC_STRUCT"]
old-location: mmc\mmc_expandsync_struct.htm
tech.root: mmc
ms.assetid: a614ea59-0661-43db-8ad5-b732d4acee80
ms.date: 12/05/2018
ms.keywords: MMC_EXPANDSYNC_STRUCT, MMC_EXPANDSYNC_STRUCT structure [MMC], _slate_mmc_expandsync_struct, mmc.mmc_expandsync_struct, mmc/MMC_EXPANDSYNC_STRUCT
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
req.typenames: MMC_EXPANDSYNC_STRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_EXPANDSYNC_STRUCT
 - mmc/_MMC_EXPANDSYNC_STRUCT
 - MMC_EXPANDSYNC_STRUCT
 - mmc/MMC_EXPANDSYNC_STRUCT
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
 - MMC_EXPANDSYNC_STRUCT
---

# MMC_EXPANDSYNC_STRUCT structure


## -description

The 
<b>MMC_EXPANDSYNC_STRUCT</b> structure is introduced in MMC 1.1.

The 
<b>MMC_EXPANDSYNC_STRUCT</b> structure contains information about a scope item that must be expanded synchronously. MMC passes a pointer to an 
<b>MMC_EXPANDSYNC_STRUCT</b> structure when it calls the snap-in's 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify">IComponentData::Notify</a> method with the 
<a href="/previous-versions/windows/desktop/mmc/mmcn-expandsync">MMCN_EXPANDSYNC</a> notification.

## -struct-fields

### -field bHandled

A value that specifies whether the snap-in has expanded the specified scope item. If this value is <b>TRUE</b>, the snap-in handles <b>MMC_EXPANDSYNC</b>, and consequently MMC does not send a further <a href="/previous-versions/windows/desktop/mmc/mmcn-expand">MMCN_EXPAND</a> notification to the snap-in.

The default value for <b>bHandled</b> is <b>FALSE</b>. If the snap-in does not handle <b>MMC_EXPANDSYNC</b> or sets <b>bHandled</b> to <b>FALSE</b>, MMC sends an <a href="/previous-versions/windows/desktop/mmc/mmcn-expand">MMCN_EXPAND</a> notification to the snap-in.

### -field bExpanding

A value that specifies whether the snap-in is expanding or collapsing. <b>TRUE</b> if the folder is being expanded. <b>FALSE</b> if the folder is being collapsed.

### -field hItem

The <b>HSCOPEITEM</b> of the item that must be expanded.

## -remarks

The <a href="/previous-versions/windows/desktop/mmc/mmcn-expandsync">MMCN_EXPANDSYNC</a> notification is sent by MMC when it requires a scope item to be synchronously expanded. Normally, this occurs when a console file is reloaded with a scope item expanded. For more information about handling this notification, see 
<b>MMCN_EXPANDSYNC</b>.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-icomponentdata-notify">IComponentData::Notify</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsolenamespace2">IConsoleNameSpace2</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-expand">MMCN_EXPAND</a>



<a href="/previous-versions/windows/desktop/mmc/mmcn-expandsync">MMCN_EXPANDSYNC</a>
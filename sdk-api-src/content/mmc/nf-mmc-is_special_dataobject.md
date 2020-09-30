---
UID: NF:mmc.IS_SPECIAL_DATAOBJECT
title: IS_SPECIAL_DATAOBJECT macro (mmc.h)
description: Determines whether an LPDATAOBJECT passed by MMC in a call to the snap-in's Notify method is a special type of data object instead of a pointer to an actual IDataObject object.
helpviewer_keywords: ["IS_SPECIAL_DATAOBJECT","IS_SPECIAL_DATAOBJECT macro [MMC]","_slate_is_special_dataobject","mmc.is_special_dataobject","mmc/IS_SPECIAL_DATAOBJECT"]
old-location: mmc\is_special_dataobject.htm
tech.root: mmc
ms.assetid: 63bc378a-b0ef-44d2-834a-f9fc4ab71e99
ms.date: 12/05/2018
ms.keywords: IS_SPECIAL_DATAOBJECT, IS_SPECIAL_DATAOBJECT macro [MMC], _slate_is_special_dataobject, mmc.is_special_dataobject, mmc/IS_SPECIAL_DATAOBJECT
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IS_SPECIAL_DATAOBJECT
 - mmc/IS_SPECIAL_DATAOBJECT
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
 - IS_SPECIAL_DATAOBJECT
---

# IS_SPECIAL_DATAOBJECT macro


## -description

The 
<b>IS_SPECIAL_DATAOBJECT</b> macro determines whether an <b>LPDATAOBJECT</b> passed by MMC in a call to the snap-in's 
Notify method is a special type of data object instead of a pointer to an actual 
<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> object.

## -parameters

### -param d

A value of type <b>LPDATAOBJECT</b> to be evaluated.

## -remarks

MMC can pass <b>DOBJ_CUSTOMOCX</b> or <b>DOBJ_CUSTOMWEB</b> as the data object in the following methods with the following notifications:

<ul>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-iextendcontrolbar-controlbarnotify">IExtendControlbar::ControlbarNotify</a>
<dl>
<dd>
<a href="/previous-versions/windows/desktop/mmc/mmcn-btn-click">MMCN_BTN_CLICK</a>
</dd>
</dl>
</li>
<li>
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-notify">IComponent::Notify</a>
<dl>
<dd>
<a href="/previous-versions/windows/desktop/mmc/mmcn-btn-click">MMCN_BTN_CLICK</a> with <i>param</i> set to<b> MMC_VERB_PROPERTIES</b></dd>
<dd>
<a href="/previous-versions/windows/desktop/mmc/mmcn-delete">MMCN_DELETE</a>
</dd>
<dd>
<a href="/previous-versions/windows/desktop/mmc/mmcn-paste">MMCN_PASTE</a>
</dd>
<dd>
<a href="/previous-versions/windows/desktop/mmc/mmcn-print">MMCN_PRINT</a>
</dd>
<dd>
<a href="/previous-versions/windows/desktop/mmc/mmcn-refresh">MMCN_REFRESH</a>
</dd>
</dl>
</li>
</ul>
If you have custom views (webpage, custom OCX, or taskpad), you can use this macro to verify that the notifications listed above pass a pointer to a data object or one of the special values, and then handle them appropriately.
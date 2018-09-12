---
UID: NF:mmc.IS_SPECIAL_DATAOBJECT
title: IS_SPECIAL_DATAOBJECT macro
author: windows-sdk-content
description: Determines whether an LPDATAOBJECT passed by MMC in a call to the snap-in's Notify method is a special type of data object instead of a pointer to an actual IDataObject object.
old-location: mmc\is_special_dataobject.htm
tech.root: mmc
ms.assetid: 63bc378a-b0ef-44d2-834a-f9fc4ab71e99
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IS_SPECIAL_DATAOBJECT, IS_SPECIAL_DATAOBJECT macro [MMC], _slate_is_special_dataobject, mmc.is_special_dataobject, mmc/IS_SPECIAL_DATAOBJECT
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - IS_SPECIAL_DATAOBJECT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IS_SPECIAL_DATAOBJECT macro


## -description


The 
<b>IS_SPECIAL_DATAOBJECT</b> macro determines whether an <b>LPDATAOBJECT</b> passed by MMC in a call to the snap-in's 
Notify method is a special type of data object instead of a pointer to an actual 
<a href="_ole_idataobject">IDataObject</a> object.


## -parameters




### -param d

A value of type <b>LPDATAOBJECT</b> to be evaluated.


## -remarks



MMC can pass <b>DOBJ_CUSTOMOCX</b> or <b>DOBJ_CUSTOMWEB</b> as the data object in the following methods with the following notifications:

<ul>
<li>
<a href="https://msdn.microsoft.com/124656df-5d12-4de1-9a71-ba080ef36611">IExtendControlbar::ControlbarNotify</a>
<dl>
<dd>
<a href="https://msdn.microsoft.com/166488ab-942f-4e25-9007-b9b79aac5995">MMCN_BTN_CLICK</a>
</dd>
</dl>
</li>
<li>
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a>
<dl>
<dd>
<a href="https://msdn.microsoft.com/166488ab-942f-4e25-9007-b9b79aac5995">MMCN_BTN_CLICK</a> with <i>param</i> set to<b> MMC_VERB_PROPERTIES</b></dd>
<dd>
<a href="https://msdn.microsoft.com/eaf6c7de-2b02-4563-9392-588a74c9d744">MMCN_DELETE</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/a2eedeb8-663a-43eb-9b8b-ab419a8b3f79">MMCN_PASTE</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/74814817-f93b-476f-a477-e6b65ed229bb">MMCN_PRINT</a>
</dd>
<dd>
<a href="https://msdn.microsoft.com/c39d99f7-7e80-4bad-8494-41f7f28c83a3">MMCN_REFRESH</a>
</dd>
</dl>
</li>
</ul>
If you have custom views (webpage, custom OCX, or taskpad), you can use this macro to verify that the notifications listed above pass a pointer to a data object or one of the special values, and then handle them appropriately.




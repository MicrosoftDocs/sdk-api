---
UID: NF:mmc.IS_SPECIAL_COOKIE
title: IS_SPECIAL_COOKIE macro (mmc.h)
description: The IS_SPECIAL_COOKIE macro determines whether an MMC_COOKIE value passed by MMC in a call to the snap-in's IComponent::QueryDataObject method is a special type of cookie.
helpviewer_keywords: ["IS_SPECIAL_COOKIE","IS_SPECIAL_COOKIE macro [MMC]","_slate_is_special_cookie","mmc.is_special_cookie","mmc/IS_SPECIAL_COOKIE"]
old-location: mmc\is_special_cookie.htm
tech.root: mmc
ms.assetid: 6638474e-987a-452b-90f1-30700df34ef2
ms.date: 12/05/2018
ms.keywords: IS_SPECIAL_COOKIE, IS_SPECIAL_COOKIE macro [MMC], _slate_is_special_cookie, mmc.is_special_cookie, mmc/IS_SPECIAL_COOKIE
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
 - IS_SPECIAL_COOKIE
 - mmc/IS_SPECIAL_COOKIE
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
 - IS_SPECIAL_COOKIE
---

# IS_SPECIAL_COOKIE macro


## -description

The 
<b>IS_SPECIAL_COOKIE</b> macro determines whether an <b>MMC_COOKIE</b> value passed by MMC in a call to the snap-in's 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a> method is a special type of cookie.

## -parameters

### -param c

A value of type <b>MMC_COOKIE</b> that you want to evaluate.

## -remarks

You can use this macro to verify that the cookie passed by MMC in its call to <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-querydataobject">IComponent::QueryDataObject</a> is one of the special values, and then handle the data object appropriately based on the specific value of the cookie (<b>MMC_MULTI_SELECT_COOKIE</b> or <b>MMC_WINDOW_COOKIE</b>).
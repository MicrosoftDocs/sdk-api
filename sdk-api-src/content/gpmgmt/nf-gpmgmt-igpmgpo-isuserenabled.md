---
UID: NF:gpmgmt.IGPMGPO.IsUserEnabled
title: IGPMGPO::IsUserEnabled (gpmgmt.h)
description: Checks whether the user policies in the GPO are enabled.
helpviewer_keywords: ["GPMGPO class [GPMC]","IsUserEnabled method","IGPMGPO interface [GPMC]","IsUserEnabled method","IGPMGPO.IsUserEnabled","IGPMGPO::IsUserEnabled","IsUserEnabled","IsUserEnabled method [GPMC]","IsUserEnabled method [GPMC]","GPMGPO class","IsUserEnabled method [GPMC]","IGPMGPO interface","_win32_igpmgpo_isuserenabled","gpmc.igpmgpo_isuserenabled","gpmgmt/IGPMGPO::IsUserEnabled"]
old-location: gpmc\igpmgpo_isuserenabled.htm
tech.root: gpmc
ms.assetid: a5ed21bd-19b7-4518-97fa-6ffcd4ea80b4
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],IsUserEnabled method, IGPMGPO interface [GPMC],IsUserEnabled method, IGPMGPO.IsUserEnabled, IGPMGPO::IsUserEnabled, IsUserEnabled, IsUserEnabled method [GPMC], IsUserEnabled method [GPMC],GPMGPO class, IsUserEnabled method [GPMC],IGPMGPO interface, _win32_igpmgpo_isuserenabled, gpmc.igpmgpo_isuserenabled, gpmgmt/IGPMGPO::IsUserEnabled
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMGPO::IsUserEnabled
 - gpmgmt/IGPMGPO::IsUserEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMGPO.IsUserEnabled
 - GPMGPO.IsUserEnabled
---

# IGPMGPO::IsUserEnabled


## -description

Checks whether the user policies in the GPO are enabled.

## -parameters

### -param pvbEnabled [out]

Value that indicates whether the user policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Value that indicates whether the user policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

<h3>VB</h3>
Value that indicates whether the user policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>
---
UID: NF:gpmgmt.IGPMGPO.IsComputerEnabled
title: IGPMGPO::IsComputerEnabled (gpmgmt.h)
description: Checks whether the computer policies in the GPO are enabled.
helpviewer_keywords: ["GPMGPO class [GPMC]","IsComputerEnabled method","IGPMGPO interface [GPMC]","IsComputerEnabled method","IGPMGPO.IsComputerEnabled","IGPMGPO::IsComputerEnabled","IsComputerEnabled","IsComputerEnabled method [GPMC]","IsComputerEnabled method [GPMC]","GPMGPO class","IsComputerEnabled method [GPMC]","IGPMGPO interface","_win32_igpmgpo_iscomputerenabled","gpmc.igpmgpo_iscomputerenabled","gpmgmt/IGPMGPO::IsComputerEnabled"]
old-location: gpmc\igpmgpo_iscomputerenabled.htm
tech.root: gpmc
ms.assetid: c5e235a0-dc12-4ff5-a3ca-0f3492edb713
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],IsComputerEnabled method, IGPMGPO interface [GPMC],IsComputerEnabled method, IGPMGPO.IsComputerEnabled, IGPMGPO::IsComputerEnabled, IsComputerEnabled, IsComputerEnabled method [GPMC], IsComputerEnabled method [GPMC],GPMGPO class, IsComputerEnabled method [GPMC],IGPMGPO interface, _win32_igpmgpo_iscomputerenabled, gpmc.igpmgpo_iscomputerenabled, gpmgmt/IGPMGPO::IsComputerEnabled
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
 - IGPMGPO::IsComputerEnabled
 - gpmgmt/IGPMGPO::IsComputerEnabled
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
 - IGPMGPO.IsComputerEnabled
 - GPMGPO.IsComputerEnabled
---

# IGPMGPO::IsComputerEnabled


## -description

Checks whether the computer policies in the GPO are enabled.

## -parameters

### -param pvbEnabled [out]

Value that indicates whether the computer policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Value that indicates whether the computer policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

<h3>VB</h3>
Value that indicates whether the computer policies in the GPO are enabled. If <b>VARIANT_TRUE</b>, they are enabled.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>
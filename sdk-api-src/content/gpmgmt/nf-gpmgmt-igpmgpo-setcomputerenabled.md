---
UID: NF:gpmgmt.IGPMGPO.SetComputerEnabled
title: IGPMGPO::SetComputerEnabled (gpmgmt.h)
description: Enables or disables the computer settings in the GPO.
helpviewer_keywords: ["GPMGPO class [GPMC]","SetComputerEnabled method","IGPMGPO interface [GPMC]","SetComputerEnabled method","IGPMGPO.SetComputerEnabled","IGPMGPO::SetComputerEnabled","SetComputerEnabled","SetComputerEnabled method [GPMC]","SetComputerEnabled method [GPMC]","GPMGPO class","SetComputerEnabled method [GPMC]","IGPMGPO interface","_win32_igpmgpo_setcomputerenabled","gpmc.igpmgpo_setcomputerenabled","gpmgmt/IGPMGPO::SetComputerEnabled"]
old-location: gpmc\igpmgpo_setcomputerenabled.htm
tech.root: gpmc
ms.assetid: 22d6fd46-9d6f-455e-8f01-96fc3f44b335
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],SetComputerEnabled method, IGPMGPO interface [GPMC],SetComputerEnabled method, IGPMGPO.SetComputerEnabled, IGPMGPO::SetComputerEnabled, SetComputerEnabled, SetComputerEnabled method [GPMC], SetComputerEnabled method [GPMC],GPMGPO class, SetComputerEnabled method [GPMC],IGPMGPO interface, _win32_igpmgpo_setcomputerenabled, gpmc.igpmgpo_setcomputerenabled, gpmgmt/IGPMGPO::SetComputerEnabled
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
 - IGPMGPO::SetComputerEnabled
 - gpmgmt/IGPMGPO::SetComputerEnabled
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
 - IGPMGPO.SetComputerEnabled
 - GPMGPO.SetComputerEnabled
---

# IGPMGPO::SetComputerEnabled


## -description

Enables or disables the computer settings in the GPO.

## -parameters

### -param vbEnabled [in]

Specifies whether to enable the computer settings in the GPO.

<b>C++:  </b>If <b>VARIANT_TRUE</b>, the method enables the settings; otherwise the method disables them.

<b>Scripting:  </b>If true, the method enables the settings; otherwise the method disables them.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>
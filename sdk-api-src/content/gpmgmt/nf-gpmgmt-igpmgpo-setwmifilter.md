---
UID: NF:gpmgmt.IGPMGPO.SetWMIFilter
title: IGPMGPO::SetWMIFilter (gpmgmt.h)
description: Links the GPMWMIFilter object to the current Group Policy object (GPO). This method can also be used to unlink existing WMI filters from the GPO.
helpviewer_keywords: ["GPMGPO class [GPMC]","SetWMIFilter method","IGPMGPO interface [GPMC]","SetWMIFilter method","IGPMGPO.SetWMIFilter","IGPMGPO::SetWMIFilter","SetWMIFilter","SetWMIFilter method [GPMC]","SetWMIFilter method [GPMC]","GPMGPO class","SetWMIFilter method [GPMC]","IGPMGPO interface","_win32_igpmgpo_setwmifilter","gpmc.igpmgpo_setwmifilter","gpmgmt/IGPMGPO::SetWMIFilter"]
old-location: gpmc\igpmgpo_setwmifilter.htm
tech.root: gpmc
ms.assetid: bd086bae-9436-4612-95d6-56fe431d2c51
ms.date: 12/05/2018
ms.keywords: GPMGPO class [GPMC],SetWMIFilter method, IGPMGPO interface [GPMC],SetWMIFilter method, IGPMGPO.SetWMIFilter, IGPMGPO::SetWMIFilter, SetWMIFilter, SetWMIFilter method [GPMC], SetWMIFilter method [GPMC],GPMGPO class, SetWMIFilter method [GPMC],IGPMGPO interface, _win32_igpmgpo_setwmifilter, gpmc.igpmgpo_setwmifilter, gpmgmt/IGPMGPO::SetWMIFilter
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
 - IGPMGPO::SetWMIFilter
 - gpmgmt/IGPMGPO::SetWMIFilter
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
 - IGPMGPO.SetWMIFilter
 - GPMGPO.SetWMIFilter
---

## -description

Links the 
<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">GPMWMIFilter</a> object to the current Group Policy object (GPO). This method can also be used to unlink existing WMI filters from the GPO.

## -parameters

### -param pIGPMWMIFilter [in]

Pointer to the WMI filter to associate with the current GPO. Passing <b>NULL</b> in this parameter unlinks any existing WMI filters.

## -returns

<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmgpo">IGPMGPO</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifilter">IGPMWMIFilter</a>
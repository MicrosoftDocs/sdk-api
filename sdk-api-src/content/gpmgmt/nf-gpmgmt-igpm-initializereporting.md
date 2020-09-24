---
UID: NF:gpmgmt.IGPM.InitializeReporting
title: IGPM::InitializeReporting (gpmgmt.h)
description: The InitializeReporting method sets the location to search for .adm files. This method initializes reporting in an asynchronous manner.
helpviewer_keywords: ["GPM object [GPMC]","InitializeReporting method","IGPM interface [GPMC]","InitializeReporting method","IGPM.InitializeReporting","IGPM::InitializeReporting","InitializeReporting","InitializeReporting method [GPMC]","InitializeReporting method [GPMC]","GPM object","InitializeReporting method [GPMC]","IGPM interface","gpmc.igpm_initializereporting","gpmgmt/IGPM::InitializeReporting"]
old-location: gpmc\igpm_initializereporting.htm
tech.root: gpmc
ms.assetid: 6e9f6ac5-d6d7-4360-b722-0b22e2391d20
ms.date: 12/05/2018
ms.keywords: GPM object [GPMC],InitializeReporting method, IGPM interface [GPMC],InitializeReporting method, IGPM.InitializeReporting, IGPM::InitializeReporting, InitializeReporting, InitializeReporting method [GPMC], InitializeReporting method [GPMC],GPM object, InitializeReporting method [GPMC],IGPM interface, gpmc.igpm_initializereporting, gpmgmt/IGPM::InitializeReporting
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
 - IGPM::InitializeReporting
 - gpmgmt/IGPM::InitializeReporting
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
 - IGPM.InitializeReporting
 - GPM.InitializeReporting
---

# IGPM::InitializeReporting


## -description

The <b>InitializeReporting</b> method sets the location to search for .adm files. This method initializes reporting in an asynchronous manner.

For both Group Policy object (GPO) reporting or Resultant Set of Policy (RSOP) reporting, the Group Policy Management Console (GPMC) searches for and loads .adm files in the following order. First it searches for the specified .adm files in the specified location. Then it searches for any additional .adm files in the default location. Finally it searches  the GPO or RSoP for any additional .adm files.

## -parameters

### -param bstrAdmPath [in]

Location to search for .adm files. Use a null-terminated string.

## -returns

<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>
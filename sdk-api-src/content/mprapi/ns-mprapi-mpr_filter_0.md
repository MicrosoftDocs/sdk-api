---
UID: NS:mprapi._MPR_FILTER_0
title: MPR_FILTER_0 (mprapi.h)
description: Contains static filter configuration information.
helpviewer_keywords: ["*PMPR_FILTER_0","MPR_FILTER_0","MPR_FILTER_0 structure [RAS]","PMPR_FILTER_0","PMPR_FILTER_0 structure pointer [RAS]","mprapi/MPR_FILTER_0","mprapi/PMPR_FILTER_0","rras.mpr_filter_0"]
old-location: rras\mpr_filter_0.htm
tech.root: RRAS
ms.assetid: f930b145-554b-40ea-ace0-60978ed428c1
ms.date: 12/05/2018
ms.keywords: '*PMPR_FILTER_0, MPR_FILTER_0, MPR_FILTER_0 structure [RAS], PMPR_FILTER_0, PMPR_FILTER_0 structure pointer [RAS], mprapi/MPR_FILTER_0, mprapi/PMPR_FILTER_0, rras.mpr_filter_0'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MPR_FILTER_0, *PMPR_FILTER_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_FILTER_0
 - mprapi/_MPR_FILTER_0
 - PMPR_FILTER_0
 - mprapi/PMPR_FILTER_0
 - MPR_FILTER_0
 - mprapi/MPR_FILTER_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - MPR_FILTER_0
---

# MPR_FILTER_0 structure


## -description

The <b>MPR_FILTER_0</b> structure contains static filter configuration information.

## -struct-fields

### -field fEnable

 
A <b>BOOL</b> that specifies the state of the static filters. Set to <b>TRUE</b> if static filters are  enabled and <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigfiltergetinfo">MprConfigFilterGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigfiltersetinfo">MprConfigFilterSetInfo</a>
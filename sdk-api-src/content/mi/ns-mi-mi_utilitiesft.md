---
UID: NS:mi._MI_UtilitiesFT
title: MI_UtilitiesFT (mi.h)
description: A support structure used in the MI_ClientFT_V1 structure. Use the functions with the name prefix &quot;MI_Utilities_&quot; to manipulate these structures.
helpviewer_keywords: ["MI_UtilitiesFT","MI_UtilitiesFT structure [Windows Management Infrastructure (MI)]","mi/MI_UtilitiesFT","wmi_v2.mi_utilitiesft"]
old-location: wmi_v2\mi_utilitiesft.htm
tech.root: wmi_v2
ms.assetid: 4f82b7b3-833c-42e8-a80c-2d057fc34fe4
ms.date: 12/05/2018
ms.keywords: MI_UtilitiesFT, MI_UtilitiesFT structure [Windows Management Infrastructure (MI)], mi/MI_UtilitiesFT, wmi_v2.mi_utilitiesft
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
req.typenames: MI_UtilitiesFT
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1,   Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - _MI_UtilitiesFT
 - mi/_MI_UtilitiesFT
 - MI_UtilitiesFT
 - mi/MI_UtilitiesFT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mi.h
api_name:
 - MI_UtilitiesFT
---

# MI_UtilitiesFT structure


## -description

A support structure used in the 
   <a href="/windows/desktop/api/mi/ns-mi-mi_clientft_v1">MI_ClientFT_V1</a> structure. Use the functions with the 
   name prefix "MI_Utilities_" to manipulate these structures.

## -struct-fields

### -field MI_ErrorCategory

TBD

### -field MI_Result

TBD

### -field CimErrorFromErrorCode

Maps an operating-system specific error code to a CIM error instance. See 
   <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_utilities_cimerrorfromerrorcode">MI_Utilities_CimErrorFromErrorCode</a>.


#### - MapErrorToExtendedError

This function has been deprecated. See 
   <a href="/previous-versions/windows/desktop/legacy/hh449450(v=vs.85)">MI_Utilities_MapErrorToExtendedError</a>.

### -field MapErrorToMiErrorCategory

This function has been deprecated. See 
   <a href="/previous-versions/windows/desktop/api/mi/nf-mi-mi_utilities_maperrortomierrorcategory">MI_Utilities_MapErrorToMiErrorCategory</a>.
---
UID: NF:mi.MI_PropertySet_Clear
title: MI_PropertySet_Clear function (mi.h)
description: Removes all names from the property list. Afterwards, the count is zero. This allows property lists to be reused (without having to be destructed and reconstructed).
helpviewer_keywords: ["MI_PropertySet_Clear","MI_PropertySet_Clear function [Windows Management Infrastructure (MI)]","mi/MI_PropertySet_Clear","wmi_v2.mi_propertyset_clear"]
old-location: wmi_v2\mi_propertyset_clear.htm
tech.root: wmi_v2
ms.assetid: c5cd80b7-51bc-48dd-a49d-c3ce6d92fd55
ms.date: 12/05/2018
ms.keywords: MI_PropertySet_Clear, MI_PropertySet_Clear function [Windows Management Infrastructure (MI)], mi/MI_PropertySet_Clear, wmi_v2.mi_propertyset_clear
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
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - MI_PropertySet_Clear
 - mi/MI_PropertySet_Clear
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
 - MI_PropertySet_Clear
---

# MI_PropertySet_Clear function


## -description

Removes all names from the property list. Afterwards, the count is zero. This allows property lists to be reused (without having to be destructed  and reconstructed).

## -parameters

### -param self [in, out]

Property list to clear.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.
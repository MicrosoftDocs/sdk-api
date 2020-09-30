---
UID: NF:mi.MI_Instance_Normalize
title: MI_Instance_Normalize function (mi.h)
description: Parses an MI_Instance_ExFT structure and then retrieves the MI_InstanceFT function table.
helpviewer_keywords: ["MI_Instance_Normalize","MI_Instance_Normalize function [Windows Management Infrastructure (MI)]","mi/MI_Instance_Normalize","wmi_v2.mi_instance_normalize"]
old-location: wmi_v2\mi_instance_normalize.htm
tech.root: wmi_v2
ms.assetid: 4FE8FD63-78F4-41C8-9A72-A2E3ABDEBB86
ms.date: 12/05/2018
ms.keywords: MI_Instance_Normalize, MI_Instance_Normalize function [Windows Management Infrastructure (MI)], mi/MI_Instance_Normalize, wmi_v2.mi_instance_normalize
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
 - MI_Instance_Normalize
 - mi/MI_Instance_Normalize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mi.h
api_name:
 - MI_Instance_Normalize
---

# MI_Instance_Normalize function


## -description

Parses an <a href="/windows/desktop/api/mi/ns-mi-mi_instanceexft">MI_Instance_ExFT</a> structure and 
    then retrieves  the <a href="/windows/desktop/api/mi/ns-mi-mi_instanceft">MI_InstanceFT</a> function 
    table.

## -parameters

### -param self [in, out]

A pointer to the object that receives the function table.

## -returns

A value of the <a href="/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.

## -see-also

<a href="/previous-versions/windows/desktop/wmi_v2/mi-interfaces">MI Interfaces</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_instance">MI_Instance</a>



<a href="/windows/desktop/api/mi/ns-mi-mi_instanceft">MI_InstanceFT</a>
---
UID: NS:setupapi._SP_POWERMESSAGEWAKE_PARAMS_A
title: SP_POWERMESSAGEWAKE_PARAMS_A (setupapi.h)
author: windows-sdk-content
description: An SP_POWERMESSAGEWAKE_PARAMS structure corresponds to a DIF_POWERMESSAGEWAKE installation request.
old-location: devinst\sp_powermessagewake_params.htm
tech.root: devinst
ms.assetid: 464919bb-c146-4d29-890f-c680a1aa06b2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PSP_POWERMESSAGEWAKE_PARAMS_A, PSP_POWERMESSAGEWAKE_PARAMS, PSP_POWERMESSAGEWAKE_PARAMS structure pointer [Device and Driver Installation], SP_POWERMESSAGEWAKE_PARAMS, SP_POWERMESSAGEWAKE_PARAMS structure [Device and Driver Installation], SP_POWERMESSAGEWAKE_PARAMS_A, devinst.sp_powermessagewake_params, di-struct_ac0928d6-b3df-4bf2-8304-a6b03eaa63a8.xml, setupapi/PSP_POWERMESSAGEWAKE_PARAMS, setupapi/SP_POWERMESSAGEWAKE_PARAMS'
ms.topic: struct
f1_keywords:
- setupapi/SP_POWERMESSAGEWAKE_PARAMS
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- setupapi.h
api_name:
- SP_POWERMESSAGEWAKE_PARAMS
 - sp_powermessagewake_params_a
targetos: Windows
req.typenames: SP_POWERMESSAGEWAKE_PARAMS_A, *PSP_POWERMESSAGEWAKE_PARAMS_A
req.redist: 
ms.custom: 19H1
---

# SP_POWERMESSAGEWAKE_PARAMS_A structure


## -description


An SP_POWERMESSAGEWAKE_PARAMS structure corresponds to a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-powermessagewake">DIF_POWERMESSAGEWAKE</a> installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>.


### -field PowerMessageWake

Buffer that contains a string of custom text. Windows displays this text on the power management page of the device properties display in Device Manager.


## -remarks



Windows only sends the DIF_POWERMESSAGEWAKE request if the drivers for the device support power management.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/install/dif-powermessagewake">DIF_POWERMESSAGEWAKE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>
 

 


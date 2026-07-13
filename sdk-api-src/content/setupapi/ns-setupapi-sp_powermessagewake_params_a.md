---
UID: NS:setupapi._SP_POWERMESSAGEWAKE_PARAMS_A
title: SP_POWERMESSAGEWAKE_PARAMS_A (setupapi.h)
description: An SP_POWERMESSAGEWAKE_PARAMS structure corresponds to a DIF_POWERMESSAGEWAKE installation request. (ANSI)
helpviewer_keywords: ["*PSP_POWERMESSAGEWAKE_PARAMS_A","PSP_POWERMESSAGEWAKE_PARAMS","PSP_POWERMESSAGEWAKE_PARAMS structure pointer [Device and Driver Installation]","SP_POWERMESSAGEWAKE_PARAMS","SP_POWERMESSAGEWAKE_PARAMS structure [Device and Driver Installation]","SP_POWERMESSAGEWAKE_PARAMS_A","devinst.sp_powermessagewake_params","di-struct_ac0928d6-b3df-4bf2-8304-a6b03eaa63a8.xml","setupapi/PSP_POWERMESSAGEWAKE_PARAMS","setupapi/SP_POWERMESSAGEWAKE_PARAMS"]
old-location: devinst\sp_powermessagewake_params.htm
tech.root: devinst
ms.assetid: 464919bb-c146-4d29-890f-c680a1aa06b2
ms.date: 12/05/2018
ms.keywords: '*PSP_POWERMESSAGEWAKE_PARAMS_A, PSP_POWERMESSAGEWAKE_PARAMS, PSP_POWERMESSAGEWAKE_PARAMS structure pointer [Device and Driver Installation], SP_POWERMESSAGEWAKE_PARAMS, SP_POWERMESSAGEWAKE_PARAMS structure [Device and Driver Installation], SP_POWERMESSAGEWAKE_PARAMS_A, devinst.sp_powermessagewake_params, di-struct_ac0928d6-b3df-4bf2-8304-a6b03eaa63a8.xml, setupapi/PSP_POWERMESSAGEWAKE_PARAMS, setupapi/SP_POWERMESSAGEWAKE_PARAMS'
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
targetos: Windows
req.typenames: SP_POWERMESSAGEWAKE_PARAMS_A, *PSP_POWERMESSAGEWAKE_PARAMS_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_POWERMESSAGEWAKE_PARAMS_A
 - setupapi/_SP_POWERMESSAGEWAKE_PARAMS_A
 - PSP_POWERMESSAGEWAKE_PARAMS_A
 - setupapi/PSP_POWERMESSAGEWAKE_PARAMS_A
 - SP_POWERMESSAGEWAKE_PARAMS_A
 - setupapi/SP_POWERMESSAGEWAKE_PARAMS_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_POWERMESSAGEWAKE_PARAMS - sp_powermessagewake_params_a
---

# SP_POWERMESSAGEWAKE_PARAMS_A structure


## -description

An SP_POWERMESSAGEWAKE_PARAMS structure corresponds to a <a href="/windows-hardware/drivers/install/dif-powermessagewake">DIF_POWERMESSAGEWAKE</a> installation request.

## -struct-fields

### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>.

### -field PowerMessageWake

Buffer that contains a string of custom text. Windows displays this text on the power management page of the device properties display in Device Manager.

## -remarks

Windows only sends the DIF_POWERMESSAGEWAKE request if the drivers for the device support power management.





> [!NOTE]
> The setupapi.h header defines SP_POWERMESSAGEWAKE_PARAMS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows-hardware/drivers/install/dif-powermessagewake">DIF_POWERMESSAGEWAKE</a>



<a href="/windows/desktop/api/setupapi/ns-setupapi-sp_classinstall_header">SP_CLASSINSTALL_HEADER</a>

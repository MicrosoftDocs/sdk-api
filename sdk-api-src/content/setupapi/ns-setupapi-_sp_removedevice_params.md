---
UID: NS:setupapi._SP_REMOVEDEVICE_PARAMS
title: "_SP_REMOVEDEVICE_PARAMS"
author: windows-sdk-content
description: An SP_REMOVEDEVICE_PARAMS structure corresponds to the DIF_REMOVE installation request.
old-location: devinst\sp_removedevice_params.htm
old-project: devinst
ms.assetid: 08d3a5c7-9350-4fb3-8476-fb22e34d7054
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: "*PSP_REMOVEDEVICE_PARAMS, PSP_REMOVEDEVICE_PARAMS, PSP_REMOVEDEVICE_PARAMS structure pointer [Device and Driver Installation], SP_REMOVEDEVICE_PARAMS, SP_REMOVEDEVICE_PARAMS structure [Device and Driver Installation], _SP_REMOVEDEVICE_PARAMS, devinst.sp_removedevice_params, di-struct_a1c87aad-2f81-4545-a088-1dadc98372d7.xml, setupapi/PSP_REMOVEDEVICE_PARAMS, setupapi/SP_REMOVEDEVICE_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: setupapi.h
req.include-header: Setupapi.h
req.redist: 
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
tech.root: 
req.typenames: SP_REMOVEDEVICE_PARAMS, *PSP_REMOVEDEVICE_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - setupapi.h
api_name:
 - SP_REMOVEDEVICE_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _SP_REMOVEDEVICE_PARAMS structure


## -description


An SP_REMOVEDEVICE_PARAMS structure corresponds to the <a href="https://msdn.microsoft.com/14429756-c059-46d7-bd1c-0ae57d1ec8b5">DIF_REMOVE</a> installation request.


## -struct-fields




### -field ClassInstallHeader

An install request header that contains the header size and the DIF code for the request. See <a href="https://msdn.microsoft.com/9f76b741-d2a7-484d-94cb-b559b017399d">SP_CLASSINSTALL_HEADER</a>. 


### -field Scope

Flags that indicate the scope of the device removal. Can be one of the following values:





#### DI_REMOVEDEVICE_GLOBAL

Make this change in all hardware profiles. Remove information about the device from the registry.



#### DI_REMOVEDEVICE_CONFIGSPECIFIC

Make this change to only the hardware profile specified by <b>HwProfile</b>. this flag only applies to root-enumerated devices. When Windows removes the device from the last hardware profile in which it was configured, Windows performs a global removal.


### -field HwProfile

The hardware profile ID for profile-specific changes. Zero specifies the current hardware profile. 


## -see-also




<a href="https://msdn.microsoft.com/14429756-c059-46d7-bd1c-0ae57d1ec8b5">DIF_REMOVE</a>



<a href="https://msdn.microsoft.com/9f76b741-d2a7-484d-94cb-b559b017399d">SP_CLASSINSTALL_HEADER</a>



<a href="https://msdn.microsoft.com/2aa631c3-8d00-4309-a37c-efaa7eda3efa">SetupDiCallClassInstaller</a>



<a href="https://msdn.microsoft.com/1070f6cc-e5de-4f4e-8325-b412751e9fb3">SetupDiRemoveDevice</a>
 

 


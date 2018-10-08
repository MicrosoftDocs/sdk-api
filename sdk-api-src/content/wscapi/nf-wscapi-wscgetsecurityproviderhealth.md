---
UID: NF:wscapi.WscGetSecurityProviderHealth
title: WscGetSecurityProviderHealth function
author: windows-sdk-content
description: Gets the aggregate health state of the security provider categories represented by the specified WSC_SECURITY_PROVIDER enumeration values.
old-location: winprog\wscgetsecurityproviderhealth.htm
tech.root: devnotes
ms.assetid: 1193eba3-a01b-4ee3-a83d-25dcdbc15de0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: WscGetSecurityProviderHealth, WscGetSecurityProviderHealth function [Windows API], winprog.wscgetsecurityproviderhealth, wscapi/WscGetSecurityProviderHealth
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wscapi.dll
api_name:
 - WscGetSecurityProviderHealth
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WscGetSecurityProviderHealth function


## -description


Gets the aggregate health state of the security provider categories represented by the specified <a href="https://msdn.microsoft.com/b32664f4-9a1d-4fd2-ab2b-e3c5a8ddf187">WSC_SECURITY_PROVIDER</a> enumeration values.


## -parameters




### -param Providers [in]

One or more of the values in the <a href="https://msdn.microsoft.com/b32664f4-9a1d-4fd2-ab2b-e3c5a8ddf187">WSC_SECURITY_PROVIDER</a> enumeration. To specify more than one value, combine the individual values by performing a bitwise OR operation.


### -param pHealth [out]

A pointer to a variable that takes the value of one of the members of the <a href="https://msdn.microsoft.com/a5f34088-13b9-4269-a3ca-777e0bb9b655">WSC_SECURITY_PROVIDER_HEALTH</a> enumeration. If more than one provider is specified in the <i>Providers</i> parameter, the value of this parameter is the health of the least healthy of the specified provider categories.


## -returns



Returns <b>S_OK</b> if the function succeeds, otherwise returns an error code. If the WSC service is not running, the return value is always <b>S_FALSE</b> and the <i>pHealth</i> out parameter is always set to <b>WSC_SECURITY_PROVIDER_HEALTH_POOR</b>.




## -see-also




<a href="https://msdn.microsoft.com/a5f34088-13b9-4269-a3ca-777e0bb9b655">WSC_SECURITY_PROVIDER_HEALTH</a>
 

 


---
UID: NF:wscapi.WscGetSecurityProviderHealth
title: WscGetSecurityProviderHealth function (wscapi.h)
description: Gets the aggregate health state of the security provider categories represented by the specified WSC_SECURITY_PROVIDER enumeration values.
helpviewer_keywords: ["WscGetSecurityProviderHealth","WscGetSecurityProviderHealth function [Windows API]","winprog.wscgetsecurityproviderhealth","wscapi/WscGetSecurityProviderHealth"]
old-location: winprog\wscgetsecurityproviderhealth.htm
tech.root: winprog
ms.assetid: 1193eba3-a01b-4ee3-a83d-25dcdbc15de0
ms.date: 12/05/2018
ms.keywords: WscGetSecurityProviderHealth, WscGetSecurityProviderHealth function [Windows API], winprog.wscgetsecurityproviderhealth, wscapi/WscGetSecurityProviderHealth
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WscGetSecurityProviderHealth
 - wscapi/WscGetSecurityProviderHealth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wscapi.dll
api_name:
 - WscGetSecurityProviderHealth
---

# WscGetSecurityProviderHealth function


## -description

Gets the aggregate health state of the security provider categories represented by the specified <a href="/windows/desktop/api/wscapi/ne-wscapi-wsc_security_provider">WSC_SECURITY_PROVIDER</a> enumeration values.

## -parameters

### -param Providers [in]

One or more of the values in the <a href="/windows/desktop/api/wscapi/ne-wscapi-wsc_security_provider">WSC_SECURITY_PROVIDER</a> enumeration. To specify more than one value, combine the individual values by performing a bitwise OR operation.

### -param pHealth [out]

A pointer to a variable that takes the value of one of the members of the <a href="/windows/desktop/api/wscapi/ne-wscapi-wsc_security_provider_health">WSC_SECURITY_PROVIDER_HEALTH</a> enumeration. If more than one provider is specified in the <i>Providers</i> parameter, the value of this parameter is the health of the least healthy of the specified provider categories.

## -returns

Returns <b>S_OK</b> if the function succeeds, otherwise returns an error code. If the WSC service is not running, the return value is always <b>S_FALSE</b> and the <i>pHealth</i> out parameter is always set to <b>WSC_SECURITY_PROVIDER_HEALTH_POOR</b>.

## -remarks

> [!NOTE]
> [WSC_SECURITY_PROVIDER::WSC_SECURITY_PROVIDER_ANTISPYWARE](/windows/desktop/api/wscapi/ne-wscapi-wsc_security_provider) should be used only in operating systems prior to Windows 10, version 1607. As of Windows 10, version 1607, WSC continues to track the status for antivirus, but not for anti-spyware.

## -see-also

<a href="/windows/desktop/api/wscapi/ne-wscapi-wsc_security_provider_health">WSC_SECURITY_PROVIDER_HEALTH</a>
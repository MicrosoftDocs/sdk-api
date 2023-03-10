---
UID: NE:wscapi._WSC_SECURITY_PROVIDER
title: WSC_SECURITY_PROVIDER (wscapi.h)
description: Defines all the services that are monitored by Windows Security Center (WSC).
helpviewer_keywords: ["*PWSC_SECURITY_PROVIDER","WSC_SECURITY_PROVIDER","WSC_SECURITY_PROVIDER enumeration [Windows API]","WSC_SECURITY_PROVIDER","*PWSC_SECURITY_PROVIDER","WSC_SECURITY_PROVIDER","*PWSC_SECURITY_PROVIDER enumeration [Windows API]","WSC_SECURITY_PROVIDER_ALL","WSC_SECURITY_PROVIDER_ANTISPYWARE","WSC_SECURITY_PROVIDER_ANTIVIRUS","WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS","WSC_SECURITY_PROVIDER_FIREWALL","WSC_SECURITY_PROVIDER_INTERNET_SETTINGS","WSC_SECURITY_PROVIDER_NONE","WSC_SECURITY_PROVIDER_SERVICE","WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL","winprog.wsc_security_provider","wscapi/WSC_SECURITY_PROVIDER","wscapi/WSC_SECURITY_PROVIDER_ALL","wscapi/WSC_SECURITY_PROVIDER_ANTISPYWARE","wscapi/WSC_SECURITY_PROVIDER_ANTIVIRUS","wscapi/WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS","wscapi/WSC_SECURITY_PROVIDER_FIREWALL","wscapi/WSC_SECURITY_PROVIDER_INTERNET_SETTINGS","wscapi/WSC_SECURITY_PROVIDER_NONE","wscapi/WSC_SECURITY_PROVIDER_SERVICE","wscapi/WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL"]
old-location: winprog\wsc_security_provider.htm
tech.root: winprog
ms.assetid: b32664f4-9a1d-4fd2-ab2b-e3c5a8ddf187
ms.date: 12/05/2018
ms.keywords: '*PWSC_SECURITY_PROVIDER, WSC_SECURITY_PROVIDER, WSC_SECURITY_PROVIDER enumeration [Windows API], WSC_SECURITY_PROVIDER,*PWSC_SECURITY_PROVIDER, WSC_SECURITY_PROVIDER,*PWSC_SECURITY_PROVIDER enumeration [Windows API], WSC_SECURITY_PROVIDER_ALL, WSC_SECURITY_PROVIDER_ANTISPYWARE, WSC_SECURITY_PROVIDER_ANTIVIRUS, WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS, WSC_SECURITY_PROVIDER_FIREWALL, WSC_SECURITY_PROVIDER_INTERNET_SETTINGS, WSC_SECURITY_PROVIDER_NONE, WSC_SECURITY_PROVIDER_SERVICE, WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL, winprog.wsc_security_provider, wscapi/WSC_SECURITY_PROVIDER, wscapi/WSC_SECURITY_PROVIDER_ALL, wscapi/WSC_SECURITY_PROVIDER_ANTISPYWARE, wscapi/WSC_SECURITY_PROVIDER_ANTIVIRUS, wscapi/WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS, wscapi/WSC_SECURITY_PROVIDER_FIREWALL, wscapi/WSC_SECURITY_PROVIDER_INTERNET_SETTINGS, wscapi/WSC_SECURITY_PROVIDER_NONE, wscapi/WSC_SECURITY_PROVIDER_SERVICE, wscapi/WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSC_SECURITY_PROVIDER, *PWSC_SECURITY_PROVIDER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSC_SECURITY_PROVIDER
 - wscapi/_WSC_SECURITY_PROVIDER
 - PWSC_SECURITY_PROVIDER
 - wscapi/PWSC_SECURITY_PROVIDER
 - WSC_SECURITY_PROVIDER
 - wscapi/WSC_SECURITY_PROVIDER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wscapi.h
api_name:
 - WSC_SECURITY_PROVIDER, *PWSC_SECURITY_PROVIDER
---

# WSC_SECURITY_PROVIDER enumeration


## -description

Defines all the services that are monitored by Windows Security Center (WSC).

## -enum-fields

### -field WSC_SECURITY_PROVIDER_FIREWALL:0x1

The aggregation of all firewalls for this computer.

### -field WSC_SECURITY_PROVIDER_AUTOUPDATE_SETTINGS:0x2

The automatic update settings for this computer.

### -field WSC_SECURITY_PROVIDER_ANTIVIRUS:0x4

The aggregation of all antivirus products for this computer.

### -field WSC_SECURITY_PROVIDER_ANTISPYWARE:0x8

The aggregation of all anti-spyware products for this computer.

### -field WSC_SECURITY_PROVIDER_INTERNET_SETTINGS:0x10

The settings that restrict the access of web sites in each of the Internet zones for this computer.

### -field WSC_SECURITY_PROVIDER_USER_ACCOUNT_CONTROL:0x20

The User Account Control (UAC) settings for this computer.

### -field WSC_SECURITY_PROVIDER_SERVICE:0x40

The running state of the WSC service on this computer.

### -field WSC_SECURITY_PROVIDER_NONE:0

None of the items that WSC monitors.

### -field WSC_SECURITY_PROVIDER_ALL

All of the items that the WSC monitors.

## -remarks

> [!NOTE]
> [WSC_SECURITY_PROVIDER::WSC_SECURITY_PROVIDER_ANTISPYWARE](/windows/desktop/api/wscapi/ne-wscapi-wsc_security_provider) should be used only in operating systems prior to Windows 10, version 1607. As of Windows 10, version 1607, WSC continues to track the status for antivirus, but not for anti-spyware.

## -see-also

<a href="/windows/desktop/api/wscapi/nf-wscapi-wscgetsecurityproviderhealth">WscGetSecurityProviderHealth</a>

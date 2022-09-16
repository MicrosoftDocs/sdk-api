---
UID: NF:wldp.WldpGetLockdownPolicy
tech.root: security
title: WldpGetLockdownPolicy
ms.date: 08/23/2022
targetos: Windows
description: Calls the library to get the security state relative to the host, and script or msi to be used.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: wldp.dll
req.header: wldp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: wldp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - wldp.dll
api_name:
 - WldpGetLockdownPolicy
f1_keywords:
 - WldpGetLockdownPolicy
 - wldp/WldpGetLockdownPolicy
dev_langs:
 - c++
helpviewer_keywords:
 - WldpGetLockdownPolicy
---

## -description

Calls the library to get the security state relative to the host, and script or msi to be used. The function has no associated import library. You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.

## -parameters

### -param hostInformation

A [**WLDP\_HOST\_INFORMATION**](ns-wldp-wldp_host_information.md) structure identifying the host and source file to be evaluated.

### -param lockdownState


Provides the resulting policy secure value. If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled. You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.

### -param lockdownFlags

The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.

## -returns

This method returns S\_OK if successful or a failure code otherwise.

## -remarks

> [!NOTE]
> [WldpCanExecuteBuffer](nf-wldp-wldpcanexecutebuffer.md), [WldpCanExecuteFile](nf-wldp-wldpcanexecutefile.md), and [WldpCanExecuteStream](nf-wldp-wldpcanexecutestream.md) are newer APIs that enable the same scenarios as **WldpGetLockdownPolicy** but with an improved implementation.

When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.

When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.

The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.

## -see-also


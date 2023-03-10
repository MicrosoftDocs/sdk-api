---
UID: NF:avrfsdk.VerifierIsPerUserSettingsEnabled
title: VerifierIsPerUserSettingsEnabled function (avrfsdk.h)
description: Determines whether Application Verifier can use per-user settings.
helpviewer_keywords: ["VerifierIsPerUserSettingsEnabled","VerifierIsPerUserSettingsEnabled function [Windows API]","avrfsdk/VerifierIsPerUserSettingsEnabled","winprog.verifierisperusersettingsenabled"]
old-location: winprog\verifierisperusersettingsenabled.htm
tech.root: winprog
ms.assetid: 29ea23ca-cb11-4b88-8863-9893e94f4e20
ms.date: 12/05/2018
ms.keywords: VerifierIsPerUserSettingsEnabled, VerifierIsPerUserSettingsEnabled function [Windows API], avrfsdk/VerifierIsPerUserSettingsEnabled, winprog.verifierisperusersettingsenabled
req.header: avrfsdk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Verifier.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VerifierIsPerUserSettingsEnabled
 - avrfsdk/VerifierIsPerUserSettingsEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Verifier.dll
api_name:
 - VerifierIsPerUserSettingsEnabled
---

# VerifierIsPerUserSettingsEnabled function


## -description

Determines whether Application Verifier can use per-user settings.



## -returns

If per-user settings are enabled, the function returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

## -remarks

Application Verifier settings are stored in the following registry key <b>HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\Image File Execution Options</b> for native applications and <b>HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Windows NT\CurrentVersion\Image File Execution Options</b> for applications running under WOW64. Only administrators can write to these keys.

Starting with Windows Vista, Application Verifier settings can be stored in <b>HKEY_CURRENT_USER</b>. To enable the use of the per-user settings, the administrator must create a REG_DWORD value named <b>ImageExecutionOptions</b> in the <b>HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Session Manager</b> key, set the low-order bit, and reboot the computer. To disable the use of the per-user settings, the administrator must either clear the bit or delete the registry value and reboot the computer.

This function has no associated import library. You must use the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> function to load Verifier.dll and call the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> function to get the address of this function.

---
UID: NF:accountssettingspaneinterop.IAccountsSettingsPaneInterop.GetForWindow
tech.root: winrt
title: IAccountsSettingsPaneInterop::GetForWindow
ms.date: 04/16/2021
targetos: Windows
description: Gets an [AccountsSettingsPane](/uwp/api/windows.ui.applicationsettings.accountssettingspane) object for the window of the active application.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: accountssettingspaneinterop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - accountssettingspaneinterop.h
api_name:
 - IAccountsSettingsPaneInterop::GetForWindow
f1_keywords:
 - IAccountsSettingsPaneInterop::GetForWindow
 - accountssettingspaneinterop/IAccountsSettingsPaneInterop::GetForWindow
dev_langs:
 - c++
---

## -description

Gets an [AccountsSettingsPane](/uwp/api/windows.ui.applicationsettings.accountssettingspane) object for the window of the active application.

## -parameters

### -param appWindow

Handle to the window of the active application.

### -param riid

The GUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example: 

`__uuidof(AccountSettingsPanel)` 

### -param accountsSettingsPane

Address of a pointer to a [AccountSettingsPane](/uwp/api/Windows.UI.ApplicationSettings.AccountsSettingsPane) object.

## -returns

If this function succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

## -see-also


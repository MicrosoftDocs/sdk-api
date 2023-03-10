---
UID: NF:uiviewsettingsinterop.IUIViewSettingsInterop.GetForWindow
tech.root: winrt
title: IUIViewSettingsInterop::GetForWindow
ms.date: 04/16/2021
targetos: Windows
description: Gets an [UIViewSettings](/uwp/api/Windows.UI.ViewManagement.UIViewSettings) object for the window of the active application.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: uiviewsettingsinterop.h
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
 - uiviewsettingsinterop.h
api_name:
 - IUIViewSettingsInterop::GetForWindow
f1_keywords:
 - IUIViewSettingsInterop::GetForWindow
 - uiviewsettingsinterop/IUIViewSettingsInterop::GetForWindow
dev_langs:
 - c++
---

## -description

Gets an [UIViewSettings](/uwp/api/Windows.UI.ViewManagement.UIViewSettings) object for the window of the active application.

## -parameters

### -param hwnd

Handle to the window of the active application.

### -param riid

The GUID for the resource interface.

The REFIID, or GUID, of the interface to the resource can be obtained by using the __uuidof() macro. For example: 

`__uuidof(UIViewSettings)` 

### -param ppv

Address of a pointer to a [UIViewSettings](/uwp/api/Windows.UI.ViewManagement.UIViewSettings) object.

## -returns

If this function succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.


## -remarks

## -see-also

[UIViewSettings](/uwp/api/Windows.UI.ViewManagement.UIViewSettings)

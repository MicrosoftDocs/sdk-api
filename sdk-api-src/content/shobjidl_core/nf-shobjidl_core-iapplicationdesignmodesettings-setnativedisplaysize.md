---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.SetNativeDisplaySize
title: IApplicationDesignModeSettings::SetNativeDisplaySize (shobjidl_core.h)
description: Sets a spoofed native display size to be used for a Windows Store app running in design mode.
helpviewer_keywords: ["IApplicationDesignModeSettings interface [Windows Shell]","SetNativeDisplaySize method","IApplicationDesignModeSettings.SetNativeDisplaySize","IApplicationDesignModeSettings::SetNativeDisplaySize","SetNativeDisplaySize","SetNativeDisplaySize method [Windows Shell]","SetNativeDisplaySize method [Windows Shell]","IApplicationDesignModeSettings interface","shell.IApplicationDesignModeSettings_SetNativeDisplaySize","shobjidl_core/IApplicationDesignModeSettings::SetNativeDisplaySize"]
old-location: shell\IApplicationDesignModeSettings_SetNativeDisplaySize.htm
tech.root: shell
ms.assetid: fc301573-6550-4e21-b82b-7800bbf34ea6
ms.date: 12/05/2018
ms.keywords: IApplicationDesignModeSettings interface [Windows Shell],SetNativeDisplaySize method, IApplicationDesignModeSettings.SetNativeDisplaySize, IApplicationDesignModeSettings::SetNativeDisplaySize, SetNativeDisplaySize, SetNativeDisplaySize method [Windows Shell], SetNativeDisplaySize method [Windows Shell],IApplicationDesignModeSettings interface, shell.IApplicationDesignModeSettings_SetNativeDisplaySize, shobjidl_core/IApplicationDesignModeSettings::SetNativeDisplaySize
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Twinapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IApplicationDesignModeSettings::SetNativeDisplaySize
 - shobjidl_core/IApplicationDesignModeSettings::SetNativeDisplaySize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Twinapi.dll
api_name:
 - IApplicationDesignModeSettings.SetNativeDisplaySize
---

# IApplicationDesignModeSettings::SetNativeDisplaySize


## -description

Sets a spoofed native display size to be used for a Windows Store app running in design mode.

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method. For a code example, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects#winui-3-with-c).

<b>SetNativeDisplaySize</b> must be called before calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-computeapplicationsize">ComputeApplicationSize</a>.

## -parameters

### -param nativeDisplaySizePixels [in]

The native size of the display to spoof, as a <a href="/windows/win32/api/windef/ns-windef-size">SIZE</a> structure. The specified size will be normalized to a landscape orientation. To spoof orientation, see <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate">SetApplicationViewState</a>.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">IInitializeWithWindow::Initialize</a> has not been called to set a proxy core window.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MONITOR_RESOLUTION_TOO_LOW </b></dt>
</dl>
</td>
<td width="60%">
You cannot launch or switch to an immersive app when the resolution is this low. This is currently defined as any resolution below 800 horizontal or 600 vertical pixels when in landscape orientation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings">IApplicationDesignModeSettings</a>
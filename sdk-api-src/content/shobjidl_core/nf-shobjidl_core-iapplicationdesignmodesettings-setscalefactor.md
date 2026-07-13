---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.SetScaleFactor
title: IApplicationDesignModeSettings::SetScaleFactor (shobjidl_core.h)
description: Sets a spoofed device scale factor to be used for a Windows Store app running in design mode.
helpviewer_keywords: ["IApplicationDesignModeSettings interface [Windows Shell]","SetScaleFactor method","IApplicationDesignModeSettings.SetScaleFactor","IApplicationDesignModeSettings::SetScaleFactor","SetScaleFactor","SetScaleFactor method [Windows Shell]","SetScaleFactor method [Windows Shell]","IApplicationDesignModeSettings interface","shell.IApplicationDesignModeSettings_SetScaleFactor","shobjidl_core/IApplicationDesignModeSettings::SetScaleFactor"]
old-location: shell\IApplicationDesignModeSettings_SetScaleFactor.htm
tech.root: shell
ms.assetid: 55b80010-a71e-44c2-8105-e9f5b9a833f5
ms.date: 12/05/2018
ms.keywords: IApplicationDesignModeSettings interface [Windows Shell],SetScaleFactor method, IApplicationDesignModeSettings.SetScaleFactor, IApplicationDesignModeSettings::SetScaleFactor, SetScaleFactor, SetScaleFactor method [Windows Shell], SetScaleFactor method [Windows Shell],IApplicationDesignModeSettings interface, shell.IApplicationDesignModeSettings_SetScaleFactor, shobjidl_core/IApplicationDesignModeSettings::SetScaleFactor
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
 - IApplicationDesignModeSettings::SetScaleFactor
 - shobjidl_core/IApplicationDesignModeSettings::SetScaleFactor
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
 - IApplicationDesignModeSettings.SetScaleFactor
---

# IApplicationDesignModeSettings::SetScaleFactor


## -description

Sets a spoofed device scale factor to be used for a Windows Store app running in design mode.

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method. For a code example, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects#winui-3-with-c).

<b>SetScaleFactor</b> must be called before calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-computeapplicationsize">ComputeApplicationSize</a>.

## -parameters

### -param scaleFactor [in]

One of the <a href="/windows/desktop/api/shtypes/ne-shtypes-device_scale_factor">DEVICE_SCALE_FACTOR</a> enumeration values that indicates the device scale factor to spoof.

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
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdesignmodesettings">IApplicationDesignModeSettings</a>
---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.ComputeApplicationSize
title: IApplicationDesignModeSettings::ComputeApplicationSize (shobjidl_core.h)
description: Gets the size of the Windows Store app, based on the current set of spoofed settings.
helpviewer_keywords: ["ComputeApplicationSize","ComputeApplicationSize method [Windows Shell]","ComputeApplicationSize method [Windows Shell]","IApplicationDesignModeSettings interface","IApplicationDesignModeSettings interface [Windows Shell]","ComputeApplicationSize method","IApplicationDesignModeSettings.ComputeApplicationSize","IApplicationDesignModeSettings::ComputeApplicationSize","shell.IApplicationDesignModeSettings_ComputeApplicationSize","shobjidl_core/IApplicationDesignModeSettings::ComputeApplicationSize"]
old-location: shell\IApplicationDesignModeSettings_ComputeApplicationSize.htm
tech.root: shell
ms.assetid: 1ac42bb8-1c24-4369-8d0d-db3ad4062501
ms.date: 12/05/2018
ms.keywords: ComputeApplicationSize, ComputeApplicationSize method [Windows Shell], ComputeApplicationSize method [Windows Shell],IApplicationDesignModeSettings interface, IApplicationDesignModeSettings interface [Windows Shell],ComputeApplicationSize method, IApplicationDesignModeSettings.ComputeApplicationSize, IApplicationDesignModeSettings::ComputeApplicationSize, shell.IApplicationDesignModeSettings_ComputeApplicationSize, shobjidl_core/IApplicationDesignModeSettings::ComputeApplicationSize
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
 - IApplicationDesignModeSettings::ComputeApplicationSize
 - shobjidl_core/IApplicationDesignModeSettings::ComputeApplicationSize
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
 - IApplicationDesignModeSettings.ComputeApplicationSize
---

# IApplicationDesignModeSettings::ComputeApplicationSize


## -description

Gets the size of the Windows Store app, based on the current set of spoofed settings.

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method. For a code example, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects#winui-3-with-c).

In addition, each of these methods must be called before calling <b>ComputeApplicationSize</b>, or the call will fail.

<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setapplicationviewstate">SetApplicationViewState</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setnativedisplaysize">SetNativeDisplaySize</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-setscalefactor">SetScaleFactor</a>
</li>
</ul>

## -parameters

### -param applicationSizePixels [out]

When this method returns successfully, receives a pointer to the size that the Windows Store app should occupy, based on the current set of spoofed settings.

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
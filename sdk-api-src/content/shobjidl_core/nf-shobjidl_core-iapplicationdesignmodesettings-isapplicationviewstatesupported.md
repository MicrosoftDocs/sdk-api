---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.IsApplicationViewStateSupported
title: IApplicationDesignModeSettings::IsApplicationViewStateSupported (shobjidl_core.h)
description: Determines whether a particular application view state is supported for specific spoofed display size and scale factor settings.
helpviewer_keywords: ["IApplicationDesignModeSettings interface [Windows Shell]","IsApplicationViewStateSupported method","IApplicationDesignModeSettings.IsApplicationViewStateSupported","IApplicationDesignModeSettings::IsApplicationViewStateSupported","IsApplicationViewStateSupported","IsApplicationViewStateSupported method [Windows Shell]","IsApplicationViewStateSupported method [Windows Shell]","IApplicationDesignModeSettings interface","shell.IApplicationDesignModeSettings_IsApplicationViewStateSupported","shobjidl_core/IApplicationDesignModeSettings::IsApplicationViewStateSupported"]
old-location: shell\IApplicationDesignModeSettings_IsApplicationViewStateSupported.htm
tech.root: shell
ms.assetid: 49661f00-15bc-48c0-a302-b81bee61180a
ms.date: 12/05/2018
ms.keywords: IApplicationDesignModeSettings interface [Windows Shell],IsApplicationViewStateSupported method, IApplicationDesignModeSettings.IsApplicationViewStateSupported, IApplicationDesignModeSettings::IsApplicationViewStateSupported, IsApplicationViewStateSupported, IsApplicationViewStateSupported method [Windows Shell], IsApplicationViewStateSupported method [Windows Shell],IApplicationDesignModeSettings interface, shell.IApplicationDesignModeSettings_IsApplicationViewStateSupported, shobjidl_core/IApplicationDesignModeSettings::IsApplicationViewStateSupported
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
 - IApplicationDesignModeSettings::IsApplicationViewStateSupported
 - shobjidl_core/IApplicationDesignModeSettings::IsApplicationViewStateSupported
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
 - IApplicationDesignModeSettings.IsApplicationViewStateSupported
---

# IApplicationDesignModeSettings::IsApplicationViewStateSupported


## -description

Determines whether a particular application view state is supported for specific spoofed display size and scale factor settings.

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method. For a code example, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects#winui-3-with-c).

## -parameters

### -param viewState [in]

One of the enumeration values that indicates the application view state for which support is being determined.

### -param nativeDisplaySizePixels [in]

The native size of the display to spoof.

### -param scaleFactor [in]

One of the enumeration values that indicates the device scale factor to spoof.

### -param supported [out]

When this method returns successfully, receives a pointer to a Boolean value which is set to <b>TRUE</b> if the application view state is supported for the given display size and scale factor, and <b>FALSE</b> if it is not.

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
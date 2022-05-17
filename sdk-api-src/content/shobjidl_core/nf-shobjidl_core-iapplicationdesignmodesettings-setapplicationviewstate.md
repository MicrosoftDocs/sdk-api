---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.SetApplicationViewState
title: IApplicationDesignModeSettings::SetApplicationViewState (shobjidl_core.h)
description: Sets a spoofed application view state (full-screen landscape, full-screen portrait, filled, or snapped) to be used for a Windows Store app running in design mode.
helpviewer_keywords: ["IApplicationDesignModeSettings interface [Windows Shell]","SetApplicationViewState method","IApplicationDesignModeSettings.SetApplicationViewState","IApplicationDesignModeSettings::SetApplicationViewState","SetApplicationViewState","SetApplicationViewState method [Windows Shell]","SetApplicationViewState method [Windows Shell]","IApplicationDesignModeSettings interface","shell.IApplicationDesignModeSettings_SetApplicationViewState","shobjidl_core/IApplicationDesignModeSettings::SetApplicationViewState"]
old-location: shell\IApplicationDesignModeSettings_SetApplicationViewState.htm
tech.root: shell
ms.assetid: 37e1845c-a58a-4da3-b259-bbf5bbf5ff6d
ms.date: 12/05/2018
ms.keywords: IApplicationDesignModeSettings interface [Windows Shell],SetApplicationViewState method, IApplicationDesignModeSettings.SetApplicationViewState, IApplicationDesignModeSettings::SetApplicationViewState, SetApplicationViewState, SetApplicationViewState method [Windows Shell], SetApplicationViewState method [Windows Shell],IApplicationDesignModeSettings interface, shell.IApplicationDesignModeSettings_SetApplicationViewState, shobjidl_core/IApplicationDesignModeSettings::SetApplicationViewState
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
 - IApplicationDesignModeSettings::SetApplicationViewState
 - shobjidl_core/IApplicationDesignModeSettings::SetApplicationViewState
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
 - IApplicationDesignModeSettings.SetApplicationViewState
---

# IApplicationDesignModeSettings::SetApplicationViewState


## -description

Sets a spoofed application view state (full-screen landscape, full-screen portrait, filled, or snapped) to be used for a Windows Store app running in design mode.

You must call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinitializewithwindow-initialize">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method. For a code example, see [Display WinRT UI objects that depend on CoreWindow](/windows/apps/develop/ui-input/display-ui-objects#winui-3-with-c).

<b>SetApplicationViewState</b> must be called before calling <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdesignmodesettings-computeapplicationsize">ComputeApplicationSize</a>.

## -parameters

### -param viewState [in]

One of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_state">APPLICATION_VIEW_STATE</a> enumeration values that indicates the application view state to spoof.

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
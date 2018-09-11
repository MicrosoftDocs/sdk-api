---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.SetNativeDisplaySize
title: IApplicationDesignModeSettings::SetNativeDisplaySize
author: windows-sdk-content
description: Sets a spoofed native display size to be used for a Windows Store app running in design mode.
old-location: shell\IApplicationDesignModeSettings_SetNativeDisplaySize.htm
tech.root: shell
ms.assetid: fc301573-6550-4e21-b82b-7800bbf34ea6
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IApplicationDesignModeSettings interface [Windows Shell],SetNativeDisplaySize method, IApplicationDesignModeSettings.SetNativeDisplaySize, IApplicationDesignModeSettings::SetNativeDisplaySize, SetNativeDisplaySize, SetNativeDisplaySize method [Windows Shell], SetNativeDisplaySize method [Windows Shell],IApplicationDesignModeSettings interface, shell.IApplicationDesignModeSettings_SetNativeDisplaySize, shobjidl_core/IApplicationDesignModeSettings::SetNativeDisplaySize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Twinapi.dll
api_name:
 - IApplicationDesignModeSettings.SetNativeDisplaySize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings::SetNativeDisplaySize


## -description


Sets a spoofed native display size to be used for a Windows Store app running in design mode.

You must call <a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method.

<b>SetNativeDisplaySize</b> must be called before calling <a href="https://msdn.microsoft.com/1ac42bb8-1c24-4369-8d0d-db3ad4062501">ComputeApplicationSize</a>.


## -parameters




### -param nativeDisplaySizePixels [in]

The native size of the display to spoof, as a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure. The specified size will be normalized to a landscape orientation. To spoof orientation, see <a href="https://msdn.microsoft.com/37e1845c-a58a-4da3-b259-bbf5bbf5ff6d">SetApplicationViewState</a>.


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

<a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">IInitializeWithWindow::Initialize</a> has not been called to set a proxy core window.

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




<a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a>
 

 


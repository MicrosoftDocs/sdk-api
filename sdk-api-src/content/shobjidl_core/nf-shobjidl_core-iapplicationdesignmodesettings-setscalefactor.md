---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.SetScaleFactor
title: IApplicationDesignModeSettings::SetScaleFactor
author: windows-sdk-content
description: Sets a spoofed device scale factor to be used for a Windows Store app running in design mode.
old-location: shell\IApplicationDesignModeSettings_SetScaleFactor.htm
tech.root: shell
ms.assetid: 55b80010-a71e-44c2-8105-e9f5b9a833f5
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IApplicationDesignModeSettings interface [Windows Shell],SetScaleFactor method, IApplicationDesignModeSettings.SetScaleFactor, IApplicationDesignModeSettings::SetScaleFactor, SetScaleFactor, SetScaleFactor method [Windows Shell], SetScaleFactor method [Windows Shell],IApplicationDesignModeSettings interface, shell.IApplicationDesignModeSettings_SetScaleFactor, shobjidl_core/IApplicationDesignModeSettings::SetScaleFactor
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
 - IApplicationDesignModeSettings.SetScaleFactor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings::SetScaleFactor


## -description


Sets a spoofed device scale factor to be used for a Windows Store app running in design mode.

You must call <a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method.

<b>SetScaleFactor</b> must be called before calling <a href="https://msdn.microsoft.com/1ac42bb8-1c24-4369-8d0d-db3ad4062501">ComputeApplicationSize</a>.


## -parameters




### -param scaleFactor [in]

One of the <a href="https://msdn.microsoft.com/DB42E7D5-4E42-4b78-89F8-0B76320E2C5F">DEVICE_SCALE_FACTOR</a> enumeration values that indicates the device scale factor to spoof.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a>
 

 


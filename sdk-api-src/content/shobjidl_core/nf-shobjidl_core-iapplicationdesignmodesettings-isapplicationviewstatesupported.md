---
UID: NF:shobjidl_core.IApplicationDesignModeSettings.IsApplicationViewStateSupported
title: IApplicationDesignModeSettings::IsApplicationViewStateSupported
author: windows-sdk-content
description: Determines whether a particular application view state is supported for specific spoofed display size and scale factor settings.
old-location: shell\IApplicationDesignModeSettings_IsApplicationViewStateSupported.htm
tech.root: shell
ms.assetid: 49661f00-15bc-48c0-a302-b81bee61180a
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IApplicationDesignModeSettings interface [Windows Shell],IsApplicationViewStateSupported method, IApplicationDesignModeSettings.IsApplicationViewStateSupported, IApplicationDesignModeSettings::IsApplicationViewStateSupported, IsApplicationViewStateSupported, IsApplicationViewStateSupported method [Windows Shell], IsApplicationViewStateSupported method [Windows Shell],IApplicationDesignModeSettings interface, shell.IApplicationDesignModeSettings_IsApplicationViewStateSupported, shobjidl_core/IApplicationDesignModeSettings::IsApplicationViewStateSupported
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
 - IApplicationDesignModeSettings.IsApplicationViewStateSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IApplicationDesignModeSettings::IsApplicationViewStateSupported


## -description


Determines whether a particular application view state is supported for specific spoofed display size and scale factor settings.

You must call <a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">IInitializeWithWindow::Initialize</a> to set a proxy core window before calling this method.


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

<a href="https://msdn.microsoft.com/429E5D12-9ED9-4f4f-A0E6-F95953C9113A">IInitializeWithWindow::Initialize</a> has not been called to set a proxy core window.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/D26C9A87-8C29-4029-BF8A-E0566DC2DF2A">IApplicationDesignModeSettings</a>
 

 


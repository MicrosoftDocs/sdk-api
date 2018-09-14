---
UID: NF:directxmath.XMVerifyCPUSupport
title: XMVerifyCPUSupport function
author: windows-sdk-content
description: Indicates if the DirectXMath Library supports the current platform.
old-location: dxmath\xmverifycpusupport.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.utilities.XMVerifyCPUSupport
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: Use DirectX..XMVerifyCPUSupport, XMVerifyCPUSupport, XMVerifyCPUSupport method [DirectX Math Support APIs], dxmath.xmverifycpusupport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Use DirectX.
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMVerifyCPUSupport
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XMVerifyCPUSupport function


## -description


Indicates if the DirectXMath Library supports the current platform.


## -parameters






## -returns



Returns true if the DirectXMath Library supports a given platform; false if it does not.




## -remarks



This is a run-time check of processor support and should be called at startup of the program before any DirectXMath
   functions or types are used.

On Windows, this function is implemented using
   <a href="http://msdn.microsoft.com/en-us/library/ms724482(VS.85).aspx">IsProcessorFeaturePresent</a>.

Therefore, when executed on windows, <code>XMVerifyCPUSupport</code> shares platform support requirements of
   <code>IsProcessorFeaturePresent</code>.

<div class="alert"><b>Note</b>  To avoid a hard dependancy on windows.h, if <i>IsProcessorFeaturePresent</i> is not defined this function always returns
   <code>false</code>. Be sure to include "windows.h" before "directxmath.h" in any module where you are calling this function.</div>
<div> </div>
<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/4d46fd96-55ca-cb66-f878-caf7894535ae">DirectXMath Library Utility Functions</a>
 

 


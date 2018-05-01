---
UID: NC:winstring.PINSPECT_HSTRING_CALLBACK
title: PINSPECT_HSTRING_CALLBACK
author: windows-driver-content
description: Provides a function pointer to the callback used by the WindowsInspectString function.
old-location: winrt\pinspect_hstring_callback.htm
old-project: WinRT
ms.assetid: B3DAB59B-15A5-42A0-8545-94F585D8FF09
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PINSPECT_HSTRING_CALLBACK, PINSPECT_HSTRING_CALLBACK function pointer [Windows Runtime], winrt.pinspect_hstring_callback, winstring/PINSPECT_HSTRING_CALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: winstring.h
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
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSAVERSION, *PWSAVERSION, *LPWSAVERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	winstring.h
api_name:
-	PINSPECT_HSTRING_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# PINSPECT_HSTRING_CALLBACK callback


## -description


Provides a function pointer to the callback used by the <a href="https://msdn.microsoft.com/DB1A35D3-D7DF-439F-B4C2-9510FC1977E9">WindowsInspectString</a> function.


## -parameters




### -param *context [in]

Custom context data provided to the <a href="https://msdn.microsoft.com/DB1A35D3-D7DF-439F-B4C2-9510FC1977E9">WindowsInspectString</a> function.


### -param readAddress [in]

The address to read data from.


### -param length [in]

The number of bytes to read, starting at <i>readAddress</i>. 


### -param *buffer [out]

The buffer that receives a copy of the bytes that are read.


## -returns



If this function pointer succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implement this callback when you use the <a href="https://msdn.microsoft.com/DB1A35D3-D7DF-439F-B4C2-9510FC1977E9">WindowsInspectString</a> function.  You can do a cross-process read, read from a dump file, or read from a remote debug debugging session.




## -see-also




<a href="https://msdn.microsoft.com/DB1A35D3-D7DF-439F-B4C2-9510FC1977E9">WindowsInspectString</a>
 

 


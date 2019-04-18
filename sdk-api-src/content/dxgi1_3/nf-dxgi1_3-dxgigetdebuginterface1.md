---
UID: NF:dxgi1_3.DXGIGetDebugInterface1
title: DXGIGetDebugInterface1 function (dxgi1_3.h)
author: windows-sdk-content
description: Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).
old-location: direct3ddxgi\dxgigetdebuginterface1.htm
tech.root: direct3ddxgi
ms.assetid: 0FE0EAF5-3ADC-426F-9DA9-FEDEC519EEF0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DXGIGetDebugInterface1, DXGIGetDebugInterface1 function [DXGI], direct3ddxgi.dxgigetdebuginterface1, dxgi1_3/DXGIGetDebugInterface1
ms.topic: function
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: Dxgi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - dxgi.dll
api_name:
 - DXGIGetDebugInterface1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DXGIGetDebugInterface1 function


## -description


Retrieves an interface that Windows Store apps use for debugging the Microsoft DirectX Graphics Infrastructure (DXGI).


## -parameters




### -param Flags

Not used.


### -param riid

The globally unique identifier (GUID) of the requested interface type, which can be the identifier for the <a href="https://msdn.microsoft.com/7DCA4750-A397-4B5A-908F-A046427D30FB">IDXGIDebug</a>, <a href="https://msdn.microsoft.com/16D52CA2-1495-407C-9B88-CF4D4C90BAFA">IDXGIDebug1</a>, or <a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a> interfaces.


### -param pDebug [out]

A pointer to a buffer that receives a pointer to the debugging interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>DXGIGetDebugInterface1</b> function returns  <b>E_NOINTERFACE</b> on systems without the Windows Software Development Kit (SDK) installed, because it's a development-time aid.




## -see-also




<a href="https://msdn.microsoft.com/209d2e65-b118-47a7-aece-fb140fdede3f">DXGI Functions</a>



<a href="https://msdn.microsoft.com/16D52CA2-1495-407C-9B88-CF4D4C90BAFA">IDXGIDebug1</a>
 

 


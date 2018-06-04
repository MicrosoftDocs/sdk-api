---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
 

 


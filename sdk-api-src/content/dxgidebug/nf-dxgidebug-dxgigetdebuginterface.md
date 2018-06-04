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

# DXGIGetDebugInterface function


## -description


Retrieves a debugging interface.


## -parameters




### -param riid

The globally unique identifier (GUID) of the requested interface type.


### -param ppDebug

A pointer to a buffer that receives a pointer to the debugging interface.


## -returns



Returns S_OK if successful; an error code otherwise. For a list of error codes, see <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -remarks




<a href="https://msdn.microsoft.com/7DCA4750-A397-4B5A-908F-A046427D30FB">IDXGIDebug</a> and <a href="https://msdn.microsoft.com/F1BC6752-F334-4E8C-BE42-B731635A799D">IDXGIInfoQueue</a> are debugging interfaces.

To access <b>DXGIGetDebugInterface</b>, call the <a href="https://msdn.microsoft.com/29514410-89fe-4888-8b34-0c30d5af237f">GetModuleHandle</a> function to get Dxgidebug.dll and the <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> function to get the address of <b>DXGIGetDebugInterface</b>.<b>Windows 8.1:  </b>Starting in Windows 8.1, Windows Store apps call the <a href="https://msdn.microsoft.com/0FE0EAF5-3ADC-426F-9DA9-FEDEC519EEF0">DXGIGetDebugInterface1</a> function to get an  <a href="https://msdn.microsoft.com/16D52CA2-1495-407C-9B88-CF4D4C90BAFA">IDXGIDebug1</a> interface.



<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/209d2e65-b118-47a7-aece-fb140fdede3f">DXGI Functions</a>



<a href="https://msdn.microsoft.com/7DCA4750-A397-4B5A-908F-A046427D30FB">IDXGIDebug</a>
 

 


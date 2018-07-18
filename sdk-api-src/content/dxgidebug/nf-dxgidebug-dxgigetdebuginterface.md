---
UID: NF:dxgidebug.DXGIGetDebugInterface
title: DXGIGetDebugInterface function
author: windows-sdk-content
description: Retrieves a debugging interface.
old-location: direct3ddxgi\dxgigetdebuginterface.htm
old-project: direct3ddxgi
ms.assetid: 7702B842-6808-4CA9-A5B4-B1A1DC2479A7
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: DXGIGetDebugInterface, DXGIGetDebugInterface function [DXGI], direct3ddxgi.dxgigetdebuginterface, dxgidebug/DXGIGetDebugInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dxgidebug.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DXGI_INFO_QUEUE_MESSAGE_SEVERITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dxgidebug.dll
api_name:
 - DXGIGetDebugInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: Dxgidebug.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
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
 

 


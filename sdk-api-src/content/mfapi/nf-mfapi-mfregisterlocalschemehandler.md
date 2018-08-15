---
UID: NF:mfapi.MFRegisterLocalSchemeHandler
title: MFRegisterLocalSchemeHandler function
author: windows-sdk-content
description: Registers a scheme handler in the caller's process.
old-location: mf\mfregisterlocalschemehandler.htm
old-project: medfound
ms.assetid: B0F14D11-D896-4CFC-8914-087611347BEB
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: MFRegisterLocalSchemeHandler, MFRegisterLocalSchemeHandler function [Media Foundation], mf.mfregisterlocalschemehandler, mfapi/MFRegisterLocalSchemeHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mfapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MF_CUSTOM_DECODE_UNIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfplat.dll
api_name:
 - MFRegisterLocalSchemeHandler
product: Windows
targetos: Windows
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# MFRegisterLocalSchemeHandler function


## -description


Registers a scheme handler in the caller's process.


## -parameters




### -param szScheme [in]

A string that contains the scheme. The scheme includes the trailing ':' character; for example, 
      "http:".


### -param pActivate [in]

A pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface of an activation 
      object. The caller implements this interface. The 
      <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> 
      method of the activation object must create a scheme handler object. The scheme handler exposes the 
      <a href="https://msdn.microsoft.com/a342054e-2cb5-494a-a2f7-d144c72d1fa5">IMFSchemeHandler</a> interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Scheme handlers are used in Microsoft Media Foundation during the source resolution process, which creates a media 
    source from a URL. For more information, see 
    <a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>.

Within a process, local scheme handlers take precedence over scheme handlers that are registered in the 
    registry. Local scheme handlers are not visible to other processes.

Use this function if you want to register a custom scheme handler for your application, but do not want the 
    handler available to other applications.




## -see-also




<a href="https://msdn.microsoft.com/B41FAA50-9CF7-4DD0-8571-1817C7C49276">MFRegisterLocalByteStreamHandler</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/b0113527-f22c-4519-b1cf-fea54bff4090">Scheme Handlers and Byte-Stream Handlers</a>
 

 


---
UID: NF:mfapi.MFRegisterLocalSchemeHandler
title: MFRegisterLocalSchemeHandler function (mfapi.h)
description: Registers a scheme handler in the caller's process.helpviewer_keywords: ["MFRegisterLocalSchemeHandler","MFRegisterLocalSchemeHandler function [Media Foundation]","mf.mfregisterlocalschemehandler","mfapi/MFRegisterLocalSchemeHandler"]
old-location: mf\mfregisterlocalschemehandler.htm
tech.root: medfound
ms.assetid: B0F14D11-D896-4CFC-8914-087611347BEB
ms.date: 12/05/2018
ms.keywords: MFRegisterLocalSchemeHandler, MFRegisterLocalSchemeHandler function [Media Foundation], mf.mfregisterlocalschemehandler, mfapi/MFRegisterLocalSchemeHandler
f1_keywords:
- mfapi/MFRegisterLocalSchemeHandler
dev_langs:
- c++
req.header: mfapi.h
req.include-header: 
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
req.lib: Mfplat.lib
req.dll: Mfplat.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- mfplat.dll
api_name:
- MFRegisterLocalSchemeHandler
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MFRegisterLocalSchemeHandler function


## -description


Registers a scheme handler in the caller's process.


## -parameters




### -param szScheme [in]

A string that contains the scheme. The scheme includes the trailing ':' character; for example, 
      "http:".


### -param pActivate [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface of an activation 
      object. The caller implements this interface. The 
      <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> 
      method of the activation object must create a scheme handler object. The scheme handler exposes the 
      <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler">IMFSchemeHandler</a> interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Scheme handlers are used in Microsoft Media Foundation during the source resolution process, which creates a media 
    source from a URL. For more information, see 
    <a href="https://docs.microsoft.com/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>.

Within a process, local scheme handlers take precedence over scheme handlers that are registered in the 
    registry. Local scheme handlers are not visible to other processes.

Use this function if you want to register a custom scheme handler for your application, but do not want the 
    handler available to other applications.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfregisterlocalbytestreamhandler">MFRegisterLocalByteStreamHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/scheme-handlers-and-byte-stream-handlers">Scheme Handlers and Byte-Stream Handlers</a>
 

 


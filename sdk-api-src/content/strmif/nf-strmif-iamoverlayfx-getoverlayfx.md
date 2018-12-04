---
UID: NF:strmif.IAMOverlayFX.GetOverlayFX
title: IAMOverlayFX::GetOverlayFX
author: windows-sdk-content
description: The GetOverlayFX method retrieves the effects currently applied to the overlay surface, if any. The application can call this method while the filter graph is running.
old-location: dshow\iamoverlayfx_getoverlayfx.htm
tech.root: DirectShow
ms.assetid: f8232fcf-a0d8-4155-941e-8613c09b4bbf
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: GetOverlayFX, GetOverlayFX method [DirectShow], GetOverlayFX method [DirectShow],IAMOverlayFX interface, IAMOverlayFX interface [DirectShow],GetOverlayFX method, IAMOverlayFX.GetOverlayFX, IAMOverlayFX::GetOverlayFX, IAMOverlayFXGetOverlayFX, dshow.iamoverlayfx_getoverlayfx, strmif/IAMOverlayFX::GetOverlayFX
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMOverlayFX.GetOverlayFX
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMOverlayFX::GetOverlayFX


## -description



The <code>GetOverlayFX</code> method retrieves the effects currently applied to the overlay surface, if any. The application can call this method while the filter graph is running.




## -parameters




### -param lpdwOverlayFX [out]

Pointer a variable that receives a value indicating which effects, if any, are currently applied to the overlay surface. The value is a logical combination of flags from the <a href="https://msdn.microsoft.com/fa984504-5175-4b94-8a75-d294cd9546a4">AMOVERLAYFX</a> enumeration.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface. The DirectShow implementation returns S_OK if successful, or E_POINTER to indicate a <b>NULL</b> pointer argument.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6bc78464-8c9e-4016-b9aa-6589d53d45bf">IAMOverlayFX Interface</a>
 

 


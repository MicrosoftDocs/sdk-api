---
UID: NF:dxgi1_6.IDXGIOutput6.GetDesc1
title: IDXGIOutput6::GetDesc1
author: windows-driver-content
description: Get an extended description of the output that includes color characteristics and connection type.
old-location: direct3ddxgi\idxgioutput6_getdesc1.htm
old-project: direct3ddxgi
ms.assetid: DE251D64-BB41-49D7-AC46-791089502286
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetDesc1, GetDesc1 method [DXGI], GetDesc1 method [DXGI],IDXGIOutput6 interface, IDXGIOutput6 interface [DXGI],GetDesc1 method, IDXGIOutput6.GetDesc1, IDXGIOutput6::GetDesc1, direct3ddxgi.idxgioutput6_getdesc1, dxgi1_6/IDXGIOutput6::GetDesc1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi1_6.h
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
req.typenames: DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIOutput6.GetDesc1
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIOutput6::GetDesc1


## -description


Get an extended description of the output that includes color characteristics and connection type.


## -parameters




### -param pDesc [out]

Type: <b><a href="https://msdn.microsoft.com/5215EF2C-9511-4B21-B574-3447FA5896F7">DXGI_OUTPUT_DESC1</a>*</b>

A pointer to the output description (see <a href="https://msdn.microsoft.com/5215EF2C-9511-4B21-B574-3447FA5896F7">DXGI_OUTPUT_DESC1</a>).


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns a code that indicates success or failure. S_OK if successful, <a href="dxgi_error.htm">DXGI_ERROR_INVALID_CALL</a> if <i>pDesc</i> is passed in as <b>NULL</b>.




## -remarks



Some scenarios do not have well-defined values for all fields in this struct. For example, if this IDXGIOutput represents a clone/duplicate set, or if the EDID has missing or invalid data. In these cases, the OS will provide some default values that correspond to a standard SDR display.

On a high DPI desktop, <b>GetDesc1</b> returns the visualized screen size unless the app is marked high DPI aware. For info about writing DPI-aware Win32 apps, see <a href="https://msdn.microsoft.com/784e308d-904b-40ac-bf98-1a00fa1c9cf0">High DPI</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/2F04E7F1-8295-441B-9E86-65C3DE5DE75F">IDXGIOutput6</a>
 

 


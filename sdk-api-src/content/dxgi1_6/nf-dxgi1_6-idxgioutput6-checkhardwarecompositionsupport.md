---
UID: NF:dxgi1_6.IDXGIOutput6.CheckHardwareCompositionSupport
title: IDXGIOutput6::CheckHardwareCompositionSupport (dxgi1_6.h)
description: Notifies applications that hardware stretching is supported.
helpviewer_keywords: ["CheckHardwareCompositionSupport","CheckHardwareCompositionSupport method [DXGI]","CheckHardwareCompositionSupport method [DXGI]","IDXGIOutput6 interface","IDXGIOutput6 interface [DXGI]","CheckHardwareCompositionSupport method","IDXGIOutput6.CheckHardwareCompositionSupport","IDXGIOutput6::CheckHardwareCompositionSupport","direct3ddxgi.idxgioutput6_checkhardwarecompositionsupport","dxgi1_6/IDXGIOutput6::CheckHardwareCompositionSupport"]
old-location: direct3ddxgi\idxgioutput6_checkhardwarecompositionsupport.htm
tech.root: direct3ddxgi
ms.assetid: 1FFB01F3-9C12-41CE-9CF6-F130CC65A7DC
ms.date: 12/05/2018
ms.keywords: CheckHardwareCompositionSupport, CheckHardwareCompositionSupport method [DXGI], CheckHardwareCompositionSupport method [DXGI],IDXGIOutput6 interface, IDXGIOutput6 interface [DXGI],CheckHardwareCompositionSupport method, IDXGIOutput6.CheckHardwareCompositionSupport, IDXGIOutput6::CheckHardwareCompositionSupport, direct3ddxgi.idxgioutput6_checkhardwarecompositionsupport, dxgi1_6/IDXGIOutput6::CheckHardwareCompositionSupport
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - IDXGIOutput6::CheckHardwareCompositionSupport
 - dxgi1_6/IDXGIOutput6::CheckHardwareCompositionSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIOutput6.CheckHardwareCompositionSupport
---

# IDXGIOutput6::CheckHardwareCompositionSupport


## -description

Notifies applications that hardware stretching is supported.

## -parameters

### -param pFlags [out]

Type: <b>UINT*</b>

A bitfield of <a href="/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags">DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS</a> enumeration values describing which types of hardware composition are supported. The values are bitwise OR'd together.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns a code that indicates success or failure.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags">DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS enumeration</a>



<a href="/windows/desktop/api/dxgi1_6/nn-dxgi1_6-idxgioutput6">IDXGIOutput6 interface</a>
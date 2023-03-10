---
UID: NF:dxgi.IDXGIFactory1.IsCurrent
title: IDXGIFactory1::IsCurrent (dxgi.h)
description: Informs an application of the possible need to re-enumerate adapters.
helpviewer_keywords: ["IDXGIFactory1 interface [DXGI]","IsCurrent method","IDXGIFactory1.IsCurrent","IDXGIFactory1::IsCurrent","IsCurrent","IsCurrent method [DXGI]","IsCurrent method [DXGI]","IDXGIFactory1 interface","a9f61d9d-ccf9-6f3c-a7a3-9545c2b59500","direct3ddxgi.idxgifactory1_iscurrent","dxgi/IDXGIFactory1::IsCurrent"]
old-location: direct3ddxgi\idxgifactory1_iscurrent.htm
tech.root: direct3ddxgi
ms.assetid: e1337b20-85c2-48e1-9205-aa729c0d0edc
ms.date: 12/05/2018
ms.keywords: IDXGIFactory1 interface [DXGI],IsCurrent method, IDXGIFactory1.IsCurrent, IDXGIFactory1::IsCurrent, IsCurrent, IsCurrent method [DXGI], IsCurrent method [DXGI],IDXGIFactory1 interface, a9f61d9d-ccf9-6f3c-a7a3-9545c2b59500, direct3ddxgi.idxgifactory1_iscurrent, dxgi/IDXGIFactory1::IsCurrent
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory1::IsCurrent
 - dxgi/IDXGIFactory1::IsCurrent
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
 - IDXGIFactory1.IsCurrent
---

## -description

Informs an application of the possible need to re-create the factory and re-enumerate adapters.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>FALSE</b>, if a new adapter is becoming available or the current adapter is going away.
    <b>TRUE</b>, no adapter changes.

<b>IsCurrent</b> returns <b>FALSE</b> to inform the calling application to re-enumerate adapters.

## -remarks

This method is not supported by DXGI 1.0, which shipped in Windows Vista and Windows Server 2008. DXGI 1.1 support is required, which is available on 
      Windows 7, Windows Server 2008 R2, and as an update to Windows Vista with Service Pack 2 (SP2) (<a href="https://support.microsoft.com/topic/application-compatibility-update-for-windows-vista-windows-server-2008-windows-7-and-windows-server-2008-r2-february-2010-3eb7848b-9a76-85fe-98d0-729e3827ea60">KB 971644</a>) and Windows Server 2008 (<a href="https://support.microsoft.com/kb/971512/">KB 971512</a>).

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory1">IDXGIFactory1</a>

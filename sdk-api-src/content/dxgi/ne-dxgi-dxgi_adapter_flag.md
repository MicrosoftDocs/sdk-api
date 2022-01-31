---
UID: NE:dxgi.DXGI_ADAPTER_FLAG
title: DXGI_ADAPTER_FLAG (dxgi.h)
description: Identifies the type of DXGI adapter.
helpviewer_keywords: ["DXGI_ADAPTER_FLAG","DXGI_ADAPTER_FLAG enumeration [DXGI]","DXGI_ADAPTER_FLAG_FORCE_DWORD","DXGI_ADAPTER_FLAG_NONE","DXGI_ADAPTER_FLAG_REMOTE","DXGI_ADAPTER_FLAG_SOFTWARE","direct3ddxgi.DXGI_ADAPTER_FLAG","dxgi/DXGI_ADAPTER_FLAG","dxgi/DXGI_ADAPTER_FLAG_FORCE_DWORD","dxgi/DXGI_ADAPTER_FLAG_NONE","dxgi/DXGI_ADAPTER_FLAG_REMOTE","dxgi/DXGI_ADAPTER_FLAG_SOFTWARE","fe5be6dc-81d9-654f-5f9d-829d3affe8d9"]
old-location: direct3ddxgi\DXGI_ADAPTER_FLAG.htm
tech.root: direct3ddxgi
ms.assetid: 9c3c78cd-4f4e-4753-969a-54ea63583be1
ms.date: 12/05/2018
ms.keywords: DXGI_ADAPTER_FLAG, DXGI_ADAPTER_FLAG enumeration [DXGI], DXGI_ADAPTER_FLAG_FORCE_DWORD, DXGI_ADAPTER_FLAG_NONE, DXGI_ADAPTER_FLAG_REMOTE, DXGI_ADAPTER_FLAG_SOFTWARE, direct3ddxgi.DXGI_ADAPTER_FLAG, dxgi/DXGI_ADAPTER_FLAG, dxgi/DXGI_ADAPTER_FLAG_FORCE_DWORD, dxgi/DXGI_ADAPTER_FLAG_NONE, dxgi/DXGI_ADAPTER_FLAG_REMOTE, dxgi/DXGI_ADAPTER_FLAG_SOFTWARE, fe5be6dc-81d9-654f-5f9d-829d3affe8d9
req.header: dxgi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DXGI_ADAPTER_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DXGI_ADAPTER_FLAG
 - dxgi/DXGI_ADAPTER_FLAG
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DXGI.h
api_name:
 - DXGI_ADAPTER_FLAG
---

# DXGI_ADAPTER_FLAG enumeration


## -description

Identifies the type of DXGI adapter.

## -enum-fields

### -field DXGI_ADAPTER_FLAG_NONE:0

Specifies no flags.

### -field DXGI_ADAPTER_FLAG_REMOTE:1

Value always set to 0. This flag is reserved.

### -field DXGI_ADAPTER_FLAG_SOFTWARE:2

Specifies a software adapter. For more info about this flag, see <a href="/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi">new info in Windows 8 about enumerating adapters</a>.

<b>Direct3D 11:  </b>This enumeration value is supported starting with Windows 8.

### -field DXGI_ADAPTER_FLAG_FORCE_DWORD:0xffffffff

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile 
          to a size other than 32 bits. This value is not used.

## -remarks

The <b>DXGI_ADAPTER_FLAG</b> enumerated type is used by the <b>Flags</b> member of the <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_adapter_desc1">DXGI_ADAPTER_DESC1</a> or <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_adapter_desc2">DXGI_ADAPTER_DESC2</a> structure to 
      identify the type of DXGI adapter.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>

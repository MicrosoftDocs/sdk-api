---
UID: NF:d3d12.ID3D12Device1.SetResidencyPriority
title: ID3D12Device1::SetResidencyPriority (d3d12.h)
description: This method sets residency priorities of a specified list of objects.
helpviewer_keywords: ["ID3D12Device1 interface","SetResidencyPriority method","ID3D12Device1.SetResidencyPriority","ID3D12Device1::SetResidencyPriority","SetResidencyPriority","SetResidencyPriority method","SetResidencyPriority method","ID3D12Device1 interface","d3d12/ID3D12Device1::SetResidencyPriority","direct3d12.id3d12device1_setresidencypriority"]
old-location: direct3d12\id3d12device1_setresidencypriority.htm
tech.root: direct3d12
ms.assetid: C489AA41-B2FC-418D-8268-9C02E5E10E0D
ms.date: 12/05/2018
ms.keywords: ID3D12Device1 interface,SetResidencyPriority method, ID3D12Device1.SetResidencyPriority, ID3D12Device1::SetResidencyPriority, SetResidencyPriority, SetResidencyPriority method, SetResidencyPriority method,ID3D12Device1 interface, d3d12/ID3D12Device1::SetResidencyPriority, direct3d12.id3d12device1_setresidencypriority
req.header: d3d12.h
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
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12Device1::SetResidencyPriority
 - d3d12/ID3D12Device1::SetResidencyPriority
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Device1.SetResidencyPriority
---

# ID3D12Device1::SetResidencyPriority


## -description

This method sets residency priorities of a specified list of objects.

## -parameters

### -param NumObjects

Type: <b>UINT</b>

Specifies the number of objects in the <i>ppObjects</i> and <i>pPriorities</i> arrays.

### -param ppObjects [in]

Type: <b>ID3D12Pageable*</b>

Specifies an array, of length <i>NumObjects</i>, containing references to <a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12pageable">ID3D12Pageable</a> objects.

### -param pPriorities [in]

Type: <b>const <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority">D3D12_RESIDENCY_PRIORITY</a>*</b>

Specifies an array, of length <i>NumObjects</i>, of <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_residency_priority">D3D12_RESIDENCY_PRIORITY</a> values for the list of objects.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -remarks

For more information, refer to <a href="/windows/desktop/direct3d12/residency">Residency</a>.

## -see-also

<a href="/windows/desktop/api/d3d12/nn-d3d12-id3d12device1">ID3D12Device1</a>
---
UID: NF:d3d12.ID3D12DeviceRemovedExtendedData.GetAutoBreadcrumbsOutput
title: ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput
description: Retrieves the Device Removed Extended Data (DRED) auto-breadcrumbs output after device removal.
helpviewer_keywords: ["GetAutoBreadcrumbsOutput","GetAutoBreadcrumbsOutput method","ID3D12DeviceRemovedExtendedData","ID3D12DeviceRemovedExtendedData interface","ID3D12DeviceRemovedExtendedData.GetAutoBreadcrumbsOutput","ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput","d3d12/ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput","direct3d12.id3d12deviceremovedextendeddata_getautobreadcrumbsoutput"]
old-location: direct3d12\id3d12deviceremovedextendeddata_getautobreadcrumbsoutput.htm
tech.root: direct3d12
ms.date: 02/08/2019
ms.keywords: GetAutoBreadcrumbsOutput, GetAutoBreadcrumbsOutput method, ID3D12DeviceRemovedExtendedData, ID3D12DeviceRemovedExtendedData interface, ID3D12DeviceRemovedExtendedData.GetAutoBreadcrumbsOutput, ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput, d3d12/ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput, direct3d12.id3d12deviceremovedextendeddata_getautobreadcrumbsoutput
req.construct-type: function
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1903
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput
 - d3d12/ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput
dev_langs:
 - c++
topic_type:
 - apiref
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.h
api_name:
 - ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput
---

# ID3D12DeviceRemovedExtendedData::GetAutoBreadcrumbsOutput


## -description

Retrieves the Device Removed Extended Data (DRED) auto-breadcrumbs output after device removal.

## -parameters

### -param pOutput

An output parameter that takes the address of a [D3D12_DRED_AUTO_BREADCRUMBS_OUTPUT](ns-d3d12-d3d12_dred_auto_breadcrumbs_output.md) object. The object whose address is passed receives the data.

## -returns

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [HRESULT](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10). Returns **DXGI_ERROR_NOT_CURRENTLY_AVAILABLE** if the device is *not* in a removed state. Returns **DXGI_ERROR_UNSUPPORTED** if auto-breadcrumbs have not been enabled with [ID3D12DeviceRemovedExtendedDataSettings::SetAutoBreadcrumbsEnablement](nf-d3d12-id3d12deviceremovedextendeddatasettings-setautobreadcrumbsenablement.md).

## -see-also

* [ID3D12DeviceRemovedExtendedData interface](nn-d3d12-id3d12deviceremovedextendeddata.md)
* [Use DRED to diagnose GPU faults](/windows/desktop/direct3d12/use-dred)


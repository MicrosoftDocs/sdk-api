---
UID: NF:directml.IDMLDevice.CheckFeatureSupport
title: IDMLDevice::CheckFeatureSupport
description: Gets information about the optional features and capabilities that are supported by the DirectML device.
helpviewer_keywords: ["CheckFeatureSupport","CheckFeatureSupport method","CheckFeatureSupport method","IDMLDevice interface","IDMLDevice interface","CheckFeatureSupport method","IDMLDevice.CheckFeatureSupport","IDMLDevice::CheckFeatureSupport","direct3d12.idmldevice_checkfeaturesupport","directml/IDMLDevice::CheckFeatureSupport"]
old-location: direct3d12\idmldevice_checkfeaturesupport.htm
tech.root: directml
ms.assetid: 7EDF00C2-332F-4DC3-B71D-EE8CDCB7E92D
ms.date: 12/5/2018
ms.keywords: CheckFeatureSupport, CheckFeatureSupport method, CheckFeatureSupport method,IDMLDevice interface, IDMLDevice interface,CheckFeatureSupport method, IDMLDevice.CheckFeatureSupport, IDMLDevice::CheckFeatureSupport, direct3d12.idmldevice_checkfeaturesupport, directml/IDMLDevice::CheckFeatureSupport
req.header: directml.h
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
req.lib: DirectML.lib
req.dll: DirectML.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDMLDevice::CheckFeatureSupport
 - directml/IDMLDevice::CheckFeatureSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.dll
api_name:
 - IDMLDevice.CheckFeatureSupport
---

# IDMLDevice::CheckFeatureSupport


## -description

Gets information about the optional features and capabilities that are supported by the DirectML device.

## -parameters

### -param feature

Type: [**DML_FEATURE**](/windows/win32/api/directml/ne-directml-dml_feature)

A constant from the [DML_FEATURE](/windows/win32/api/directml/ne-directml-dml_feature) enumeration describing the feature(s) that you want to query for support.

### -param featureQueryDataSize

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The size of the structure pointed to by the <i>featureQueryData</i> parameter, if provided, otherwise 0.

### -param featureQueryData [in, optional]

Type: <b>const void*</b>

An optional pointer to a query structure that corresponds to the value of the <i>feature</i> parameter. To determine the corresponding query type for each constant, see [DML_FEATURE](/windows/win32/api/directml/ne-directml-dml_feature).

### -param featureSupportDataSize

Type: [**UINT**](/windows/desktop/winprog/windows-data-types)

The size of the structure pointed to by the <i>featureSupportData</i> parameter.

### -param featureSupportData [out]

Type: <b>void*</b>

A pointer to a support data structure that corresponds to the value of the <i>feature</i> parameter. To determine the corresponding support data type for each constant, see [DML_FEATURE](/windows/win32/api/directml/ne-directml-dml_feature).

## -returns

Type: [**HRESULT**](/windows/desktop/winprog/windows-data-types)

If this method succeeds, it returns **S_OK**. Otherwise, it returns **DXGI_ERROR_UNSUPPORTED** if the [DML_FEATURE](/windows/win32/api/directml/ne-directml-dml_feature) is unrecognized or unsupported, and **E_INVALIDARG** if the parameters are incorrect.

## -see-also

[IDMLDevice](/windows/win32/api/directml/nn-directml-idmldevice)

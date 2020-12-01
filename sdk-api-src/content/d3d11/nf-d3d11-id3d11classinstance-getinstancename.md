---
UID: NF:d3d11.ID3D11ClassInstance.GetInstanceName
title: ID3D11ClassInstance::GetInstanceName (d3d11.h)
description: Gets the instance name of the current HLSL class.
helpviewer_keywords: ["52fdee2c-7566-954c-edad-a7d91948caac","GetInstanceName","GetInstanceName method [Direct3D 11]","GetInstanceName method [Direct3D 11]","ID3D11ClassInstance interface","ID3D11ClassInstance interface [Direct3D 11]","GetInstanceName method","ID3D11ClassInstance.GetInstanceName","ID3D11ClassInstance::GetInstanceName","d3d11/ID3D11ClassInstance::GetInstanceName","direct3d11.id3d11classinstance_getinstancename"]
old-location: direct3d11\id3d11classinstance_getinstancename.htm
tech.root: direct3d11
ms.assetid: 9e9c3410-6421-4300-b3a6-de4840a81117
ms.date: 12/05/2018
ms.keywords: 52fdee2c-7566-954c-edad-a7d91948caac, GetInstanceName, GetInstanceName method [Direct3D 11], GetInstanceName method [Direct3D 11],ID3D11ClassInstance interface, ID3D11ClassInstance interface [Direct3D 11],GetInstanceName method, ID3D11ClassInstance.GetInstanceName, ID3D11ClassInstance::GetInstanceName, d3d11/ID3D11ClassInstance::GetInstanceName, direct3d11.id3d11classinstance_getinstancename
req.header: d3d11.h
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
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ClassInstance::GetInstanceName
 - d3d11/ID3D11ClassInstance::GetInstanceName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11ClassInstance.GetInstanceName
---

# ID3D11ClassInstance::GetInstanceName


## -description

Gets the instance name of the current HLSL class.

## -parameters

### -param pInstanceName [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPSTR</a></b>

The instance name of the current HLSL class.

### -param pBufferLength [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a>*</b>

The length of the <i>pInstanceName</i> parameter.

## -remarks

GetInstanceName will return a valid name only for instances acquired using 
          <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance">ID3D11ClassLinkage::GetClassInstance</a>.
        

For more information about using the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a> interface, see 
          <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">Dynamic Linking</a>.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>
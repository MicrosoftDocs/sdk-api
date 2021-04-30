---
UID: NF:d3d11.ID3D11ClassLinkage.GetClassInstance
title: ID3D11ClassLinkage::GetClassInstance (d3d11.h)
description: Gets the class-instance object that represents the specified HLSL class.
helpviewer_keywords: ["45d18e06-7ca3-6ff7-a95b-a56150c07b87","GetClassInstance","GetClassInstance method [Direct3D 11]","GetClassInstance method [Direct3D 11]","ID3D11ClassLinkage interface","ID3D11ClassLinkage interface [Direct3D 11]","GetClassInstance method","ID3D11ClassLinkage.GetClassInstance","ID3D11ClassLinkage::GetClassInstance","d3d11/ID3D11ClassLinkage::GetClassInstance","direct3d11.id3d11classlinkage_getclassinstance"]
old-location: direct3d11\id3d11classlinkage_getclassinstance.htm
tech.root: direct3d11
ms.assetid: 055f1670-0643-4a0a-8411-ac8a62e98826
ms.date: 12/05/2018
ms.keywords: 45d18e06-7ca3-6ff7-a95b-a56150c07b87, GetClassInstance, GetClassInstance method [Direct3D 11], GetClassInstance method [Direct3D 11],ID3D11ClassLinkage interface, ID3D11ClassLinkage interface [Direct3D 11],GetClassInstance method, ID3D11ClassLinkage.GetClassInstance, ID3D11ClassLinkage::GetClassInstance, d3d11/ID3D11ClassLinkage::GetClassInstance, direct3d11.id3d11classlinkage_getclassinstance
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ClassLinkage::GetClassInstance
 - d3d11/ID3D11ClassLinkage::GetClassInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11ClassLinkage.GetClassInstance
---

# ID3D11ClassLinkage::GetClassInstance


## -description

Gets the class-instance object that represents the specified HLSL class.

## -parameters

### -param pClassInstanceName [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of a class for which to get the class instance.

### -param InstanceIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the class instance.

### -param ppInstance [out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>**</b>

The address of a pointer to an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a> interface to initialize.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

For more information about using the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a> interface, see
          <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">Dynamic Linking</a>.
        

A class instance must have at least 1 data member in order to be available for the runtime to use with
          <b>ID3D11ClassLinkage::GetClassInstance</b>.
          Any instance with no members will be optimized out of a compiled shader blob as a zero-sized object.
          If you have a class with no data members, use
          <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance">ID3D11ClassLinkage::CreateClassInstance</a> instead.
        

<b>Windows Phone 8:
        </b> This API is supported.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classinstance">ID3D11ClassInstance</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11classlinkage">ID3D11ClassLinkage</a>
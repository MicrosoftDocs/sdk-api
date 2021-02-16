---
UID: NF:xapobase.CXAPOParametersBase.CXAPOParametersBase
title: CXAPOParametersBase::CXAPOParametersBase (xapobase.h)
description: Creates an instance of the CXAPOParametersBase class.
helpviewer_keywords: ["CXAPOParametersBase","CXAPOParametersBase interface [XAudio2 Audio Mixing APIs]","CXAPOParametersBase method","CXAPOParametersBase method [XAudio2 Audio Mixing APIs]","CXAPOParametersBase method [XAudio2 Audio Mixing APIs]","CXAPOParametersBase interface","CXAPOParametersBase.CXAPOParametersBase","CXAPOParametersBase::CXAPOParametersBase","xapobase/CXAPOParametersBase::CXAPOParametersBase","xaudio2.cxapoparametersbase_cxapoparametersbase"]
old-location: xaudio2\cxapoparametersbase_cxapoparametersbase.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.cxapoparameterbase.CXAPOParametersBase.CXAPOParametersBase(BYTE,UINT32,BOOL)
ms.date: 12/05/2018
ms.keywords: CXAPOParametersBase, CXAPOParametersBase interface [XAudio2 Audio Mixing APIs],CXAPOParametersBase method, CXAPOParametersBase method [XAudio2 Audio Mixing APIs], CXAPOParametersBase method [XAudio2 Audio Mixing APIs],CXAPOParametersBase interface, CXAPOParametersBase.CXAPOParametersBase, CXAPOParametersBase::CXAPOParametersBase, xapobase/CXAPOParametersBase::CXAPOParametersBase, xaudio2.cxapoparametersbase_cxapoparametersbase
req.header: xapobase.h
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
req.lib: XAPOBase.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CXAPOParametersBase::CXAPOParametersBase
 - xapobase/CXAPOParametersBase::CXAPOParametersBase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - XAPOBase.lib
 - XAPOBase.dll
api_name:
 - CXAPOParametersBase.CXAPOParametersBase
---

# CXAPOParametersBase::CXAPOParametersBase


## -description

Creates an instance of the <a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a> class.

## -parameters

### -param pRegistrationProperties

Type: <b>const XAPO_REGISTRATION_PROPERTIES*</b>

A pointer to an <a href="/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties">XAPO_REGISTRATION_PROPERTIES</a> structure that contains the registration properties for the XAPO.

### -param pParameterBlocks

Type: <b>BYTE*</b>

Pointer to three contiguous process parameter blocks used for synchronization.

### -param uParameterBlockByteSize

Type: <b>UINT32</b>

Size of a parameter block in <i>pParameterBlocks</i>.

### -param fProducer

Type: <b>BOOL</b>

If TRUE, indicates <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a> produces data to be returned by <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-getparameters">IXAPOParameters::GetParameters</a> and disallows calls to <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a>.

## -remarks

All process parameter blocks in <i>pParameterBlocks</i> must be initialized to the same default value before there is a call to the <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-process">IXAPO::Process</a>, <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-getparameters">IXAPOParameters::GetParameters</a>, and <a href="/windows/desktop/api/xapo/nf-xapo-ixapoparameters-setparameters">IXAPOParameters::SetParameters</a> methods. Usually this initialization should be handled in <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-initialize">IXAPO::Initialize</a> or in <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-lockforprocess">IXAPO::LockForProcess</a>.



The object created by this <a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a> will have a reference count of 1.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/api/xapobase/nl-xapobase-cxapoparametersbase">CXAPOParametersBase</a>
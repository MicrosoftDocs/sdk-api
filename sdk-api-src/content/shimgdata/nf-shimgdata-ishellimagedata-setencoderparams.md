---
UID: NF:shimgdata.IShellImageData.SetEncoderParams
title: IShellImageData::SetEncoderParams (shimgdata.h)
description: Sets encoder parameters.
helpviewer_keywords: ["IShellImageData interface [Windows Shell]","SetEncoderParams method","IShellImageData.SetEncoderParams","IShellImageData::SetEncoderParams","SetEncoderParams","SetEncoderParams method [Windows Shell]","SetEncoderParams method [Windows Shell]","IShellImageData interface","_shell_IShellImageData_SetEncoderParams","shell.IShellImageData_SetEncoderParams","shimgdata/IShellImageData::SetEncoderParams"]
old-location: shell\IShellImageData_SetEncoderParams.htm
tech.root: shell
ms.assetid: 20a5b0ab-5dcb-4ea9-9c15-d7c1e6c2c6be
ms.date: 12/05/2018
ms.keywords: IShellImageData interface [Windows Shell],SetEncoderParams method, IShellImageData.SetEncoderParams, IShellImageData::SetEncoderParams, SetEncoderParams, SetEncoderParams method [Windows Shell], SetEncoderParams method [Windows Shell],IShellImageData interface, _shell_IShellImageData_SetEncoderParams, shell.IShellImageData_SetEncoderParams, shimgdata/IShellImageData::SetEncoderParams
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageData::SetEncoderParams
 - shimgdata/IShellImageData::SetEncoderParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellImageData.SetEncoderParams
---

# IShellImageData::SetEncoderParams


## -description

Sets encoder parameters.

## -parameters

### -param pbagEnc [in]

Type: <b><a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a>*</b>

A pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> containing the encoder properties.

## -returns

Type: <b>HRESULT</b>

Always returns<b> S_OK</b>.

## -remarks

The <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> passed in <i>pbagEnc</i> is used during a save operation. The image and any edits made to it, such as <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-rotate">Rotate</a> or <a href="/windows/desktop/api/shimgdata/nf-shimgdata-ishellimagedata-scale">Scale</a>, can be saved by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for either <a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a> or <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a> and calling their <b>Save</b> method.
---
UID: NF:appxpackaging.IAppxBlockMapBlock.GetCompressedSize
title: IAppxBlockMapBlock::GetCompressedSize (appxpackaging.h)
description: Retrieves compressed size of the block.
helpviewer_keywords: ["GetCompressedSize","GetCompressedSize method [App packaging and management]","GetCompressedSize method [App packaging and management]","IAppxBlockMapBlock interface","IAppxBlockMapBlock interface [App packaging and management]","GetCompressedSize method","IAppxBlockMapBlock.GetCompressedSize","IAppxBlockMapBlock::GetCompressedSize","appxpackaging/IAppxBlockMapBlock::GetCompressedSize","appxpkg.iappxblockmapblock_getcompressedsize"]
old-location: appxpkg\iappxblockmapblock_getcompressedsize.htm
tech.root: appxpkg
ms.assetid: 02B5F96E-EA8B-407F-98D8-BF6BFF72B346
ms.date: 12/05/2018
ms.keywords: GetCompressedSize, GetCompressedSize method [App packaging and management], GetCompressedSize method [App packaging and management],IAppxBlockMapBlock interface, IAppxBlockMapBlock interface [App packaging and management],GetCompressedSize method, IAppxBlockMapBlock.GetCompressedSize, IAppxBlockMapBlock::GetCompressedSize, appxpackaging/IAppxBlockMapBlock::GetCompressedSize, appxpkg.iappxblockmapblock_getcompressedsize
req.header: appxpackaging.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: AppxPackaging.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppxBlockMapBlock::GetCompressedSize
 - appxpackaging/IAppxBlockMapBlock::GetCompressedSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - AppxPackaging.h
api_name:
 - IAppxBlockMapBlock.GetCompressedSize
---

# IAppxBlockMapBlock::GetCompressedSize


## -description

Retrieves compressed size of the block.

## -parameters

### -param size [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT32</a>*</b>

The compressed size of the block, in bytes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This size corresponds to the compressed size of the block. 

The <i>size</i> value corresponds to the <b>Size</b> attribute of the <a href="/uwp/schemas/blockmapschema/element-block">Block</a> element in the block map.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>
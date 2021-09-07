---
UID: NF:appxpackaging.IAppxBlockMapBlock.GetHash
title: IAppxBlockMapBlock::GetHash (appxpackaging.h)
description: Retrieves the hash value of the block.
helpviewer_keywords: ["GetHash","GetHash method [App packaging and management]","GetHash method [App packaging and management]","IAppxBlockMapBlock interface","IAppxBlockMapBlock interface [App packaging and management]","GetHash method","IAppxBlockMapBlock.GetHash","IAppxBlockMapBlock::GetHash","appxpackaging/IAppxBlockMapBlock::GetHash","appxpkg.iappxblockmapblock_gethash"]
old-location: appxpkg\iappxblockmapblock_gethash.htm
tech.root: appxpkg
ms.assetid: 9A8460C2-2BEE-4CEC-BAF4-779E6F58664D
ms.date: 12/05/2018
ms.keywords: GetHash, GetHash method [App packaging and management], GetHash method [App packaging and management],IAppxBlockMapBlock interface, IAppxBlockMapBlock interface [App packaging and management],GetHash method, IAppxBlockMapBlock.GetHash, IAppxBlockMapBlock::GetHash, appxpackaging/IAppxBlockMapBlock::GetHash, appxpkg.iappxblockmapblock_gethash
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
 - IAppxBlockMapBlock::GetHash
 - appxpackaging/IAppxBlockMapBlock::GetHash
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
 - IAppxBlockMapBlock.GetHash
---

# IAppxBlockMapBlock::GetHash


## -description

Retrieves the hash value of the block.

## -parameters

### -param bufferSize [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT32</a>*</b>

The length of  <i>buffer</i>.

### -param buffer [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BYTE</a>**</b>

The byte sequence representing the hash value of the block.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <i>buffer</i> value corresponds to the <b>Hash</b> attribute of the <b>Block</b> element.

The caller is responsible for deallocating the memory used for <i>buffer</i>. Use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function to deallocate the memory.

## -see-also

<a href="/windows/desktop/api/appxpackaging/nn-appxpackaging-iappxblockmapblock">IAppxBlockMapBlock</a>
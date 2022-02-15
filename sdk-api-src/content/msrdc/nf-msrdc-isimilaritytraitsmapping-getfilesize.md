---
UID: NF:msrdc.ISimilarityTraitsMapping.GetFileSize
title: ISimilarityTraitsMapping::GetFileSize (msrdc.h)
description: Returns the size of a similarity traits table file.
helpviewer_keywords: ["GetFileSize","GetFileSize method [Remote Differential Compression]","GetFileSize method [Remote Differential Compression]","ISimilarityTraitsMapping interface","ISimilarityTraitsMapping interface [Remote Differential Compression]","GetFileSize method","ISimilarityTraitsMapping.GetFileSize","ISimilarityTraitsMapping::GetFileSize","fs.isimilaritytraitsmapping_getfilesize","msrdc/ISimilarityTraitsMapping::GetFileSize","rdc.isimilaritytraitsmapping_getfilesize"]
old-location: rdc\isimilaritytraitsmapping_getfilesize.htm
tech.root: rdc
ms.assetid: 920b9c77-ca45-42ff-801f-cbe1ab3eab2c
ms.date: 12/05/2018
ms.keywords: GetFileSize, GetFileSize method [Remote Differential Compression], GetFileSize method [Remote Differential Compression],ISimilarityTraitsMapping interface, ISimilarityTraitsMapping interface [Remote Differential Compression],GetFileSize method, ISimilarityTraitsMapping.GetFileSize, ISimilarityTraitsMapping::GetFileSize, fs.isimilaritytraitsmapping_getfilesize, msrdc/ISimilarityTraitsMapping::GetFileSize, rdc.isimilaritytraitsmapping_getfilesize
req.header: msrdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MsRdc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISimilarityTraitsMapping::GetFileSize
 - msrdc/ISimilarityTraitsMapping::GetFileSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsRdc.dll
api_name:
 - ISimilarityTraitsMapping.GetFileSize
---

# ISimilarityTraitsMapping::GetFileSize


## -description

Returns the size of a similarity traits table file.

## -parameters

### -param fileSize [out]

Pointer to a location that receives the file size, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a>
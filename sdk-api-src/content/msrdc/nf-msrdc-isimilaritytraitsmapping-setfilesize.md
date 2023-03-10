---
UID: NF:msrdc.ISimilarityTraitsMapping.SetFileSize
title: ISimilarityTraitsMapping::SetFileSize (msrdc.h)
description: Sets the size of a similarity traits table file.
helpviewer_keywords: ["ISimilarityTraitsMapping interface [Remote Differential Compression]","SetFileSize method","ISimilarityTraitsMapping.SetFileSize","ISimilarityTraitsMapping::SetFileSize","SetFileSize","SetFileSize method [Remote Differential Compression]","SetFileSize method [Remote Differential Compression]","ISimilarityTraitsMapping interface","fs.isimilaritytraitsmapping_setfilesize","msrdc/ISimilarityTraitsMapping::SetFileSize","rdc.isimilaritytraitsmapping_setfilesize"]
old-location: rdc\isimilaritytraitsmapping_setfilesize.htm
tech.root: rdc
ms.assetid: 7f8afa56-6531-40dd-979f-12506ad8c286
ms.date: 12/05/2018
ms.keywords: ISimilarityTraitsMapping interface [Remote Differential Compression],SetFileSize method, ISimilarityTraitsMapping.SetFileSize, ISimilarityTraitsMapping::SetFileSize, SetFileSize, SetFileSize method [Remote Differential Compression], SetFileSize method [Remote Differential Compression],ISimilarityTraitsMapping interface, fs.isimilaritytraitsmapping_setfilesize, msrdc/ISimilarityTraitsMapping::SetFileSize, rdc.isimilaritytraitsmapping_setfilesize
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
 - ISimilarityTraitsMapping::SetFileSize
 - msrdc/ISimilarityTraitsMapping::SetFileSize
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
 - ISimilarityTraitsMapping.SetFileSize
---

# ISimilarityTraitsMapping::SetFileSize


## -description

Sets the size of a similarity traits table file.

## -parameters

### -param fileSize [in]

Pointer to a location that specifies the file size, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-isimilaritytraitsmapping">ISimilarityTraitsMapping</a>
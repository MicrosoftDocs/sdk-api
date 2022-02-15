---
UID: NF:msrdc.IRdcLibrary.ComputeDefaultRecursionDepth
title: IRdcLibrary::ComputeDefaultRecursionDepth (msrdc.h)
description: Computes the maximum level of recursion for the specified file size.
helpviewer_keywords: ["ComputeDefaultRecursionDepth","ComputeDefaultRecursionDepth method [Remote Differential Compression]","ComputeDefaultRecursionDepth method [Remote Differential Compression]","IRdcLibrary interface","IRdcLibrary interface [Remote Differential Compression]","ComputeDefaultRecursionDepth method","IRdcLibrary.ComputeDefaultRecursionDepth","IRdcLibrary::ComputeDefaultRecursionDepth","fs.irdclibrary_computedefaultrecursiondepth","msrdc/IRdcLibrary::ComputeDefaultRecursionDepth","rdc.irdclibrary_computedefaultrecursiondepth"]
old-location: rdc\irdclibrary_computedefaultrecursiondepth.htm
tech.root: rdc
ms.assetid: b42c7b46-9f3c-46d2-a6a7-b5176fc40645
ms.date: 12/05/2018
ms.keywords: ComputeDefaultRecursionDepth, ComputeDefaultRecursionDepth method [Remote Differential Compression], ComputeDefaultRecursionDepth method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],ComputeDefaultRecursionDepth method, IRdcLibrary.ComputeDefaultRecursionDepth, IRdcLibrary::ComputeDefaultRecursionDepth, fs.irdclibrary_computedefaultrecursiondepth, msrdc/IRdcLibrary::ComputeDefaultRecursionDepth, rdc.irdclibrary_computedefaultrecursiondepth
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
req.type-library: MsRdc.dll
req.lib: 
req.dll: MsRdc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRdcLibrary::ComputeDefaultRecursionDepth
 - msrdc/IRdcLibrary::ComputeDefaultRecursionDepth
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
 - IRdcLibrary.ComputeDefaultRecursionDepth
---

# IRdcLibrary::ComputeDefaultRecursionDepth


## -description

The 
   <b>ComputeDefaultRecursionDepth</b> 
 method computes the maximum level of recursion for the specified file size. The depth returned 
 by the method may be larger than <b>MSRDC_MAXIMUM_DEPTH</b>. The caller must compare the value 
 returned through the <i>depth</i> parameter with 
 <b>MSRDC_MAXIMUM_DEPTH</b>.

## -parameters

### -param fileSize [in]

The approximate size of the file.

### -param depth [out]

Pointer to a <b>ULONG</b> that will receive the suggested maximum recursion 
    depth.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdclibrary">IRdcLibrary</a>
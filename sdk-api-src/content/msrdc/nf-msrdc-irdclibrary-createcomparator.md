---
UID: NF:msrdc.IRdcLibrary.CreateComparator
title: IRdcLibrary::CreateComparator (msrdc.h)
description: Creates a signature comparator.
helpviewer_keywords: ["CreateComparator","CreateComparator method [Remote Differential Compression]","CreateComparator method [Remote Differential Compression]","IRdcLibrary interface","IRdcLibrary interface [Remote Differential Compression]","CreateComparator method","IRdcLibrary.CreateComparator","IRdcLibrary::CreateComparator","MSRDC_DEFAULT_COMPAREBUFFER","MSRDC_MAXIMUM_COMPAREBUFFER","MSRDC_MINIMUM_COMPAREBUFFER","fs.irdclibrary_createcomparator","msrdc/IRdcLibrary::CreateComparator","rdc.irdclibrary_createcomparator"]
old-location: rdc\irdclibrary_createcomparator.htm
tech.root: rdc
ms.assetid: 21e83ed0-974a-470f-8a7f-1776f1575100
ms.date: 12/05/2018
ms.keywords: CreateComparator, CreateComparator method [Remote Differential Compression], CreateComparator method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],CreateComparator method, IRdcLibrary.CreateComparator, IRdcLibrary::CreateComparator, MSRDC_DEFAULT_COMPAREBUFFER, MSRDC_MAXIMUM_COMPAREBUFFER, MSRDC_MINIMUM_COMPAREBUFFER, fs.irdclibrary_createcomparator, msrdc/IRdcLibrary::CreateComparator, rdc.irdclibrary_createcomparator
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
 - IRdcLibrary::CreateComparator
 - msrdc/IRdcLibrary::CreateComparator
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
 - IRdcLibrary.CreateComparator
---

# IRdcLibrary::CreateComparator


## -description

The <b>CreateComparator</b> method 
    creates a signature comparator.

## -parameters

### -param iSeedSignaturesFile [in]

An <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a> interface pointer initialized to 
      read the seed signatures.

### -param comparatorBufferSize [in]

Specifies the size of the comparator buffer. The range is from 
      <b>MSRDC_MINIMUM_COMPAREBUFFER</b> to 
      <b>MSRDC_MAXIMUM_COMPAREBUFFER</b>.



#### MSRDC_MINIMUM_COMPAREBUFFER (100000)

Minimum size of a comparator buffer.



#### MSRDC_DEFAULT_COMPAREBUFFER (3200000)

Default size of a comparator buffer. Used if zero (0) is passed for 
        <i>comparatorBufferSize</i>.



#### MSRDC_MAXIMUM_COMPAREBUFFER (1073741824)

Maximum size of a comparator buffer. (1&lt;&lt;30)

### -param iComparator [out]

Pointer to a location that will receive an 
      <a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdccomparator">IRdcComparator</a> interface pointer. On a successful return 
      the interface will be initialized on return. Callers must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The caller must create a separate signature comparator for each 
    level of recursion.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdccomparator">IRdcComparator</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdcfilereader">IRdcFileReader</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdclibrary">IRdcLibrary</a>
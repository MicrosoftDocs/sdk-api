---
UID: NF:msrdc.IRdcLibrary.GetRDCVersion
title: IRdcLibrary::GetRDCVersion (msrdc.h)
description: Retrieves the version of the installed RDC runtime and the oldest version of the RDC interfaces supported by the installed runtime.
helpviewer_keywords: ["GetRDCVersion","GetRDCVersion method [Remote Differential Compression]","GetRDCVersion method [Remote Differential Compression]","IRdcLibrary interface","IRdcLibrary interface [Remote Differential Compression]","GetRDCVersion method","IRdcLibrary.GetRDCVersion","IRdcLibrary::GetRDCVersion","fs.irdclibrary_getrdcversion","msrdc/IRdcLibrary::GetRDCVersion","rdc.irdclibrary_getrdcversion"]
old-location: rdc\irdclibrary_getrdcversion.htm
tech.root: rdc
ms.assetid: 3eef00e8-62d9-49bc-8340-fb56f5a4573d
ms.date: 12/05/2018
ms.keywords: GetRDCVersion, GetRDCVersion method [Remote Differential Compression], GetRDCVersion method [Remote Differential Compression],IRdcLibrary interface, IRdcLibrary interface [Remote Differential Compression],GetRDCVersion method, IRdcLibrary.GetRDCVersion, IRdcLibrary::GetRDCVersion, fs.irdclibrary_getrdcversion, msrdc/IRdcLibrary::GetRDCVersion, rdc.irdclibrary_getrdcversion
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
 - IRdcLibrary::GetRDCVersion
 - msrdc/IRdcLibrary::GetRDCVersion
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
 - IRdcLibrary.GetRDCVersion
---

# IRdcLibrary::GetRDCVersion


## -description

The <b>GetRDCVersion</b> method retrieves 
    the version of the installed RDC runtime and the oldest version of the RDC interfaces supported by the installed 
    runtime.

## -parameters

### -param currentVersion [out]

Address of a <b>ULONG</b> that will receive the installed version of RDC. This 
      corresponds to the <b>MSRDC_VERSION</b> value.

### -param minimumCompatibleAppVersion [out]

Address of a <b>ULONG</b> that will receive the oldest version of RDC supported by 
      the installed version of RDC. This corresponds to the 
      <b>MSRDC_MINIMUM_COMPATIBLE_APP_VERSION</b> value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/msrdc/nf-msrdc-irdcgeneratorparameters-getparametersversion">IRdcGeneratorParameters::GetParametersVersion</a>



<a href="/previous-versions/windows/desktop/api/msrdc/nn-msrdc-irdclibrary">IRdcLibrary</a>
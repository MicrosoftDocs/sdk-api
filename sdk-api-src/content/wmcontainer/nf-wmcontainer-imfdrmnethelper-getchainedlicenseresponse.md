---
UID: NF:wmcontainer.IMFDRMNetHelper.GetChainedLicenseResponse
title: IMFDRMNetHelper::GetChainedLicenseResponse (wmcontainer.h)
description: Not implemented in this release. (IMFDRMNetHelper.GetChainedLicenseResponse)
helpviewer_keywords: ["GetChainedLicenseResponse","GetChainedLicenseResponse method [Media Foundation]","GetChainedLicenseResponse method [Media Foundation]","IMFDRMNetHelper interface","IMFDRMNetHelper interface [Media Foundation]","GetChainedLicenseResponse method","IMFDRMNetHelper.GetChainedLicenseResponse","IMFDRMNetHelper::GetChainedLicenseResponse","mf.imfdrmnethelper_getchainedlicenseresponse","wmcontainer/IMFDRMNetHelper::GetChainedLicenseResponse"]
old-location: mf\imfdrmnethelper_getchainedlicenseresponse.htm
tech.root: mf
ms.assetid: eedbefd8-8540-4bf9-b602-6bebf089fcf7
ms.date: 12/05/2018
ms.keywords: GetChainedLicenseResponse, GetChainedLicenseResponse method [Media Foundation], GetChainedLicenseResponse method [Media Foundation],IMFDRMNetHelper interface, IMFDRMNetHelper interface [Media Foundation],GetChainedLicenseResponse method, IMFDRMNetHelper.GetChainedLicenseResponse, IMFDRMNetHelper::GetChainedLicenseResponse, mf.imfdrmnethelper_getchainedlicenseresponse, wmcontainer/IMFDRMNetHelper::GetChainedLicenseResponse
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IMFDRMNetHelper::GetChainedLicenseResponse
 - wmcontainer/IMFDRMNetHelper::GetChainedLicenseResponse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcontainer.h
api_name:
 - IMFDRMNetHelper.GetChainedLicenseResponse
---

# IMFDRMNetHelper::GetChainedLicenseResponse


## -description

Not implemented in this release.

## -parameters

### -param ppLicenseResponse [out]

Receives a pointer to a byte array that contains the license response. The caller must free the array by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

### -param pcbLicenseResponse [out]

Receives the size, in bytes, of the license response.

## -returns

The method returns <b>E_NOTIMPL</b>.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfdrmnethelper">IMFDRMNetHelper</a>

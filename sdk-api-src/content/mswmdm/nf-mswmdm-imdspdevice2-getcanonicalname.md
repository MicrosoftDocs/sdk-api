---
UID: NF:mswmdm.IMDSPDevice2.GetCanonicalName
title: IMDSPDevice2::GetCanonicalName (mswmdm.h)
description: The GetCanonicalPName method gets the canonical name of a device.
helpviewer_keywords: ["GetCanonicalName","GetCanonicalName method [windows Media Device Manager]","GetCanonicalName method [windows Media Device Manager]","IMDSPDevice2 interface","IMDSPDevice2 interface [windows Media Device Manager]","GetCanonicalName method","IMDSPDevice2.GetCanonicalName","IMDSPDevice2::GetCanonicalName","IMDSPDevice2GetPnPName","mswmdm/IMDSPDevice2::GetCanonicalName","wmdm.imdspdevice2_getcanonicalname"]
old-location: wmdm\imdspdevice2_getcanonicalname.htm
tech.root: WMDM
ms.assetid: 0888c780-e358-45ae-809b-34a19d496059
ms.date: 12/05/2018
ms.keywords: GetCanonicalName, GetCanonicalName method [windows Media Device Manager], GetCanonicalName method [windows Media Device Manager],IMDSPDevice2 interface, IMDSPDevice2 interface [windows Media Device Manager],GetCanonicalName method, IMDSPDevice2.GetCanonicalName, IMDSPDevice2::GetCanonicalName, IMDSPDevice2GetPnPName, mswmdm/IMDSPDevice2::GetCanonicalName, wmdm.imdspdevice2_getcanonicalname
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPDevice2::GetCanonicalName
 - mswmdm/IMDSPDevice2::GetCanonicalName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPDevice2.GetCanonicalName
---

# IMDSPDevice2::GetCanonicalName


## -description

The <b>GetCanonicalPName</b> method gets the canonical name of a device.

## -parameters

### -param pwszPnPName [out]

A wide character, null-terminated buffer holding the canonical name. The caller allocates and releases this buffer.

### -param nMaxChars [in]

Integer containing the maximum number of characters that can be placed in <i>pwszCanonicalName</i>, including the termination character.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

## -remarks

This method returns a canonical name for the device. The service provider should return the device path name of the device as its canonical name. The service provider is passed the device path name in the <b>CreateDevice</b> method on the <a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2">IMDServiceProvider2</a> interface.

This is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2">IMDSPDevice2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider2">IMDServiceProvider2 Interface</a>



<a href="/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice">IMDServiceProvider2::CreateDevice</a>
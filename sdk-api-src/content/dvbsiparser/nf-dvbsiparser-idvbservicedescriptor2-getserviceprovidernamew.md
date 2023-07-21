---
UID: NF:dvbsiparser.IDvbServiceDescriptor2.GetServiceProviderNameW
title: IDvbServiceDescriptor2::GetServiceProviderNameW (dvbsiparser.h)
description: Gets a string containing the service provider name from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetServiceProviderNameW","GetServiceProviderNameW method [Microsoft TV Technologies]","GetServiceProviderNameW method [Microsoft TV Technologies]","IDvbServiceDescriptor2 interface","IDvbServiceDescriptor2 interface [Microsoft TV Technologies]","GetServiceProviderNameW method","IDvbServiceDescriptor2.GetServiceProviderNameW","IDvbServiceDescriptor2::GetServiceProviderNameW","dvbsiparser/IDvbServiceDescriptor2::GetServiceProviderNameW","mstv.idvbservicedescriptor2_getserviceprovidernamew"]
old-location: mstv\idvbservicedescriptor2_getserviceprovidernamew.htm
tech.root: mstv
ms.assetid: b0d44251-adef-4a90-b5a3-dc36576169b9
ms.date: 12/05/2018
ms.keywords: GetServiceProviderNameW, GetServiceProviderNameW method [Microsoft TV Technologies], GetServiceProviderNameW method [Microsoft TV Technologies],IDvbServiceDescriptor2 interface, IDvbServiceDescriptor2 interface [Microsoft TV Technologies],GetServiceProviderNameW method, IDvbServiceDescriptor2.GetServiceProviderNameW, IDvbServiceDescriptor2::GetServiceProviderNameW, dvbsiparser/IDvbServiceDescriptor2::GetServiceProviderNameW, mstv.idvbservicedescriptor2_getserviceprovidernamew
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IDvbServiceDescriptor2::GetServiceProviderNameW
 - dvbsiparser/IDvbServiceDescriptor2::GetServiceProviderNameW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbServiceDescriptor2.GetServiceProviderNameW
---

# IDvbServiceDescriptor2::GetServiceProviderNameW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a string containing the service provider name from  a Digital Video Broadcast (DVB) service descriptor.

## -parameters

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrName [out]

Receives the service provider name string as a <b>BSTR</b>. The caller must free the string by calling <b>SysFreeString</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor2">IDvbServiceDescriptor2</a>
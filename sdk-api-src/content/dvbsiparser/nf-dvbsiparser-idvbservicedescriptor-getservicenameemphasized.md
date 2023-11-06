---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceNameEmphasized
title: IDvbServiceDescriptor::GetServiceNameEmphasized (dvbsiparser.h)
description: Gets the emphasized service name from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetServiceNameEmphasized","GetServiceNameEmphasized method [Microsoft TV Technologies]","GetServiceNameEmphasized method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetServiceNameEmphasized method","IDvbServiceDescriptor.GetServiceNameEmphasized","IDvbServiceDescriptor::GetServiceNameEmphasized","dvbsiparser/IDvbServiceDescriptor::GetServiceNameEmphasized","mstv.idvbservicedescriptor_getservicenameemphasized"]
old-location: mstv\idvbservicedescriptor_getservicenameemphasized.htm
tech.root: mstv
ms.assetid: 232bdf11-b9f5-48cd-8cd5-f03cd589d43e
ms.date: 12/05/2018
ms.keywords: GetServiceNameEmphasized, GetServiceNameEmphasized method [Microsoft TV Technologies], GetServiceNameEmphasized method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceNameEmphasized method, IDvbServiceDescriptor.GetServiceNameEmphasized, IDvbServiceDescriptor::GetServiceNameEmphasized, dvbsiparser/IDvbServiceDescriptor::GetServiceNameEmphasized, mstv.idvbservicedescriptor_getservicenameemphasized
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
 - IDvbServiceDescriptor::GetServiceNameEmphasized
 - dvbsiparser/IDvbServiceDescriptor::GetServiceNameEmphasized
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
 - IDvbServiceDescriptor.GetServiceNameEmphasized
---

# IDvbServiceDescriptor::GetServiceNameEmphasized


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the emphasized service name from a Digital Video Broadcast (DVB) service descriptor.

## -parameters

### -param pbstrName [out]

Pointer to a buffer that receives the service name. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method calls <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getserviceprovidernamew">IDvbServiceDescriptor::GetServiceProviderNameW</a> to get the emphasized service name. It is provided to maintain compatibility with  the original DVB service descriptor specification.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor-getserviceprovidernamew">IDvbServiceDescriptor::GetServiceProviderNameW</a>
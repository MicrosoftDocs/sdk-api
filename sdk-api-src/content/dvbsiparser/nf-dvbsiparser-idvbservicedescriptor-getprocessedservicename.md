---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetProcessedServiceName
title: IDvbServiceDescriptor::GetProcessedServiceName (dvbsiparser.h)
description: Gets the processed service name from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetProcessedServiceName","GetProcessedServiceName method [Microsoft TV Technologies]","GetProcessedServiceName method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetProcessedServiceName method","IDvbServiceDescriptor.GetProcessedServiceName","IDvbServiceDescriptor::GetProcessedServiceName","dvbsiparser/IDvbServiceDescriptor::GetProcessedServiceName","mstv.idvbservicedescriptor_getprocessedservicename"]
old-location: mstv\idvbservicedescriptor_getprocessedservicename.htm
tech.root: mstv
ms.assetid: c0441e70-270e-4685-9107-865c2b6398e9
ms.date: 12/05/2018
ms.keywords: GetProcessedServiceName, GetProcessedServiceName method [Microsoft TV Technologies], GetProcessedServiceName method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetProcessedServiceName method, IDvbServiceDescriptor.GetProcessedServiceName, IDvbServiceDescriptor::GetProcessedServiceName, dvbsiparser/IDvbServiceDescriptor::GetProcessedServiceName, mstv.idvbservicedescriptor_getprocessedservicename
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
 - IDvbServiceDescriptor::GetProcessedServiceName
 - dvbsiparser/IDvbServiceDescriptor::GetProcessedServiceName
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
 - IDvbServiceDescriptor.GetProcessedServiceName
---

# IDvbServiceDescriptor::GetProcessedServiceName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the processed service name from a Digital Video Broadcast (DVB) service descriptor.

## -parameters

### -param pbstrName [out]

Pointer to a buffer that receives the service name. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method calls <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor2-getservicenamew">IDvbServiceDescriptor2::GetServiceNameW</a> to get the processed  service name. It is provided to maintain compatibility with  the original DVB service descriptor specification.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbservicedescriptor2-getservicenamew">IDvbServiceDescriptor2::GetServiceNameW</a>
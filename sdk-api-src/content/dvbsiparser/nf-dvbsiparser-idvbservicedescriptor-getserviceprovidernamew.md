---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceProviderNameW
title: IDvbServiceDescriptor::GetServiceProviderNameW (dvbsiparser.h)
description: Gets the service provider name string from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetServiceProviderNameW","GetServiceProviderNameW method [Microsoft TV Technologies]","GetServiceProviderNameW method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetServiceProviderNameW method","IDvbServiceDescriptor.GetServiceProviderNameW","IDvbServiceDescriptor::GetServiceProviderNameW","dvbsiparser/IDvbServiceDescriptor::GetServiceProviderNameW","mstv.idvbservicedescriptor_getserviceprovidernamew"]
old-location: mstv\idvbservicedescriptor_getserviceprovidernamew.htm
tech.root: mstv
ms.assetid: e4c6f1f1-8cf8-4848-bb88-e1d11f4fe045
ms.date: 12/05/2018
ms.keywords: GetServiceProviderNameW, GetServiceProviderNameW method [Microsoft TV Technologies], GetServiceProviderNameW method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceProviderNameW method, IDvbServiceDescriptor.GetServiceProviderNameW, IDvbServiceDescriptor::GetServiceProviderNameW, dvbsiparser/IDvbServiceDescriptor::GetServiceProviderNameW, mstv.idvbservicedescriptor_getserviceprovidernamew
f1_keywords:
- dvbsiparser/IDvbServiceDescriptor.GetServiceProviderNameW
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IDvbServiceDescriptor.GetServiceProviderNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbServiceDescriptor::GetServiceProviderNameW


## -description


 Gets the service provider name string from a Digital Video Broadcast (DVB) service descriptor.  


## -parameters




### -param pbstrName

Pointer to a buffer that receives the service provider name string. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>
 

 


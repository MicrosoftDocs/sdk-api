---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceProviderName
title: IDvbServiceDescriptor::GetServiceProviderName (dvbsiparser.h)
description: Gets the service provider name from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetServiceProviderName","GetServiceProviderName method [Microsoft TV Technologies]","GetServiceProviderName method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetServiceProviderName method","IDvbServiceDescriptor.GetServiceProviderName","IDvbServiceDescriptor::GetServiceProviderName","dvbsiparser/IDvbServiceDescriptor::GetServiceProviderName","mstv.idvbservicedescriptor_getserviceprovidername"]
old-location: mstv\idvbservicedescriptor_getserviceprovidername.htm
tech.root: mstv
ms.assetid: ea5d358f-7da3-47c4-9172-7e5c60a61f84
ms.date: 12/05/2018
ms.keywords: GetServiceProviderName, GetServiceProviderName method [Microsoft TV Technologies], GetServiceProviderName method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceProviderName method, IDvbServiceDescriptor.GetServiceProviderName, IDvbServiceDescriptor::GetServiceProviderName, dvbsiparser/IDvbServiceDescriptor::GetServiceProviderName, mstv.idvbservicedescriptor_getserviceprovidername
f1_keywords:
- dvbsiparser/IDvbServiceDescriptor.GetServiceProviderName
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
- IDvbServiceDescriptor.GetServiceProviderName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbServiceDescriptor::GetServiceProviderName


## -description


 Gets the service provider name from a Digital Video Broadcast (DVB) service descriptor. 


## -parameters




### -param pszName

Pointer to a buffer that receives the service provider name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>
 

 


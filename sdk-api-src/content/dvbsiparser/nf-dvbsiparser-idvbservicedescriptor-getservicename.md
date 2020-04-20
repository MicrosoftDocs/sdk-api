---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceName
title: IDvbServiceDescriptor::GetServiceName (dvbsiparser.h)
description: Gets the service_name field from a Digital Video Broadcast (DVB) service descriptor.helpviewer_keywords: ["GetServiceName","GetServiceName method [Microsoft TV Technologies]","GetServiceName method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetServiceName method","IDvbServiceDescriptor.GetServiceName","IDvbServiceDescriptor::GetServiceName","dvbsiparser/IDvbServiceDescriptor::GetServiceName","mstv.idvbservicedescriptor_getservicename"]
old-location: mstv\idvbservicedescriptor_getservicename.htm
tech.root: mstv
ms.assetid: d3c59ebc-fc32-49ba-86b3-5737c3af2225
ms.date: 12/05/2018
ms.keywords: GetServiceName, GetServiceName method [Microsoft TV Technologies], GetServiceName method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceName method, IDvbServiceDescriptor.GetServiceName, IDvbServiceDescriptor::GetServiceName, dvbsiparser/IDvbServiceDescriptor::GetServiceName, mstv.idvbservicedescriptor_getservicename
f1_keywords:
- dvbsiparser/IDvbServiceDescriptor.GetServiceName
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
- IDvbServiceDescriptor.GetServiceName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbServiceDescriptor::GetServiceName


## -description


Gets the service_name field  from a Digital Video Broadcast (DVB) service descriptor.  


## -parameters




### -param pszName

Pointer to a memory block that receives the service name. The caller is responsible for releasing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>
 

 


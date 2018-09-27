---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceName
title: IDvbServiceDescriptor::GetServiceName
author: windows-sdk-content
description: Gets the service_name field from a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicedescriptor_getservicename.htm
tech.root: MSTV
ms.assetid: d3c59ebc-fc32-49ba-86b3-5737c3af2225
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetServiceName, GetServiceName method [Microsoft TV Technologies], GetServiceName method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceName method, IDvbServiceDescriptor.GetServiceName, IDvbServiceDescriptor::GetServiceName, dvbsiparser/IDvbServiceDescriptor::GetServiceName, mstv.idvbservicedescriptor_getservicename
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/7024259f-3dcf-46e0-9984-d5924c9e5b54">IDvbServiceDescriptor</a>
 

 


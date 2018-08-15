---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceProviderNameW
title: IDvbServiceDescriptor::GetServiceProviderNameW
author: windows-sdk-content
description: Gets the service provider name string from a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicedescriptor_getserviceprovidernamew.htm
old-project: mstv
ms.assetid: e4c6f1f1-8cf8-4848-bb88-e1d11f4fe045
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetServiceProviderNameW, GetServiceProviderNameW method [Microsoft TV Technologies], GetServiceProviderNameW method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceProviderNameW method, IDvbServiceDescriptor.GetServiceProviderNameW, IDvbServiceDescriptor::GetServiceProviderNameW, dvbsiparser/IDvbServiceDescriptor::GetServiceProviderNameW, mstv.idvbservicedescriptor_getserviceprovidernamew
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.redist: 
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbServiceDescriptor.GetServiceProviderNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/7024259f-3dcf-46e0-9984-d5924c9e5b54">IDvbServiceDescriptor</a>
 

 


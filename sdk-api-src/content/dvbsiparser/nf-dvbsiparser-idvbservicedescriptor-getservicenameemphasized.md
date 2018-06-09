---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetServiceNameEmphasized
title: IDvbServiceDescriptor::GetServiceNameEmphasized
author: windows-sdk-content
description: Gets the emphasized service name from a Digital Video Broadcast (DVB) service descriptor.
old-location: mstv\idvbservicedescriptor_getservicenameemphasized.htm
old-project: mstv
ms.assetid: 232bdf11-b9f5-48cd-8cd5-f03cd589d43e
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetServiceNameEmphasized, GetServiceNameEmphasized method [Microsoft TV Technologies], GetServiceNameEmphasized method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetServiceNameEmphasized method, IDvbServiceDescriptor.GetServiceNameEmphasized, IDvbServiceDescriptor::GetServiceNameEmphasized, dvbsiparser/IDvbServiceDescriptor::GetServiceNameEmphasized, mstv.idvbservicedescriptor_getservicenameemphasized
ms.prod: windows
ms.technology: windows-sdk
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
 - IDvbServiceDescriptor.GetServiceNameEmphasized
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbServiceDescriptor::GetServiceNameEmphasized


## -description


 Gets the emphasized service name from a Digital Video Broadcast (DVB) service descriptor.  


## -parameters




### -param pbstrName [out]

Pointer to a buffer that receives the service name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method calls <a href="https://msdn.microsoft.com/e4c6f1f1-8cf8-4848-bb88-e1d11f4fe045">IDvbServiceDescriptor::GetServiceProviderNameW</a> to get the emphasized service name. It is provided to maintain compatibility with  the original DVB service descriptor specification.




## -see-also




<a href="https://msdn.microsoft.com/7024259f-3dcf-46e0-9984-d5924c9e5b54">IDvbServiceDescriptor</a>



<a href="https://msdn.microsoft.com/e4c6f1f1-8cf8-4848-bb88-e1d11f4fe045">IDvbServiceDescriptor::GetServiceProviderNameW</a>
 

 


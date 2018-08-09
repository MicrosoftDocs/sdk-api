---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetTag
title: IDvbMultilingualServiceNameDescriptor::GetTag
author: windows-sdk-content
description: Gets the tag identifying a Digital Video Broadcast (DVB) multilingual service name descriptor.
old-location: mstv\idvbmultilingualservicenamedescriptor_gettag.htm
old-project: mstv
ms.assetid: 428f3309-67aa-4a47-9585-0308bee47e16
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbMultilingualServiceNameDescriptor interface, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbMultilingualServiceNameDescriptor.GetTag, IDvbMultilingualServiceNameDescriptor::GetTag, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetTag, mstv.idvbmultilingualservicenamedescriptor_gettag
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
 - IDvbMultilingualServiceNameDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbMultilingualServiceNameDescriptor::GetTag


## -description


Gets the tag identifying a Digital Video Broadcast (DVB) multilingual service name descriptor. 


## -parameters




### -param pbVal [out]

Receives the service list descriptor tag. Typically, this value is 0x5D for multilingual service name descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b384ecf-aa56-476d-b347-b5438ab069fe">IDvbMultilingualServiceNameDescriptor</a>
 

 


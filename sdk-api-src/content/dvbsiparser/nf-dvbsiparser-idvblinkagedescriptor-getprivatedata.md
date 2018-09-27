---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetPrivateData
title: IDvbLinkageDescriptor::GetPrivateData
author: windows-sdk-content
description: Gets the private data from a Digital Video Broadcast (DVB) linkage descriptor.
old-location: mstv\idvblinkagedescriptor_getprivatedata.htm
tech.root: MSTV
ms.assetid: 959aeb87-b661-4567-a6fd-2d28be6b0a02
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetPrivateData, GetPrivateData method [Microsoft TV Technologies], GetPrivateData method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetPrivateData method, IDvbLinkageDescriptor.GetPrivateData, IDvbLinkageDescriptor::GetPrivateData, dvbsiparser/IDvbLinkageDescriptor::GetPrivateData, mstv.idvblinkagedescriptor_getprivatedata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IDvbLinkageDescriptor.GetPrivateData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbLinkageDescriptor::GetPrivateData


## -description


Gets the private data from a Digital Video Broadcast (DVB) linkage descriptor.


## -parameters




### -param pbLen [in, out]

On input, specifies the size of the buffer (pointed to by the <i>pbData</i> parameter) allocated for the private data, in bytes. On output, gets the actual length of the private  data that is received.


### -param pbData [out]

Receives private data from the DVB linkage descriptor.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/4e419b50-b9c2-48e4-a484-f0fcf5c9cb7f">IDvbLinkageDescriptor</a>
 

 


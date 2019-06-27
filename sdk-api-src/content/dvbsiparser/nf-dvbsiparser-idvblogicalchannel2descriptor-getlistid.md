---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListId
title: IDvbLogicalChannel2Descriptor::GetListId (dvbsiparser.h)
author: windows-sdk-content
description: Gets the identifier for a channel list from a Digital Video Broadcast (DVB) logical channel descriptor.
old-location: mstv\idvblogicalchannel2descriptor_getlistid.htm
tech.root: mstv
ms.assetid: 39f97d38-d588-43d0-8aea-6ef4e1b3440b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetListId, GetListId method [Microsoft TV Technologies], GetListId method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListId method, IDvbLogicalChannel2Descriptor.GetListId, IDvbLogicalChannel2Descriptor::GetListId, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListId, mstv.idvblogicalchannel2descriptor_getlistid
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IDvbLogicalChannel2Descriptor.GetListId"
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
 - IDvbLogicalChannel2Descriptor.GetListId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbLogicalChannel2Descriptor::GetListId


## -description


Gets the identifier for a channel list from a  Digital Video Broadcast (DVB) logical channel descriptor.


## -parameters




### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>method to get the number of channel list records in the logical channel descriptor.


### -param pbVal [out]

Pointer to a byte that receives the channel list identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchannel2descriptor">IDvbLogicalChannel2Descriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>
 

 


---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListCountOfRecords
title: IDvbLogicalChannel2Descriptor::GetListCountOfRecords
author: windows-sdk-content
description: Gets an indexed count of records for a channel list in a Digital Video Broadcast (DVB) logical channel descriptor.
old-location: mstv\idvblogicalchannel2descriptor_getlistcountofrecords.htm
old-project: mstv
ms.assetid: ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetListCountOfRecords, GetListCountOfRecords method [Microsoft TV Technologies], GetListCountOfRecords method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListCountOfRecords method, IDvbLogicalChannel2Descriptor.GetListCountOfRecords, IDvbLogicalChannel2Descriptor::GetListCountOfRecords, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountOfRecords, mstv.idvblogicalchannel2descriptor_getlistcountofrecords
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbLogicalChannel2Descriptor.GetListCountOfRecords
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLogicalChannel2Descriptor::GetListCountOfRecords


## -description


Gets an indexed count of records for a channel list in a Digital Video Broadcast (DVB) logical channel descriptor.


## -parameters




### -param bChannelListIndex [in]

Specifies the channel list number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/97cadf6c-2549-4a7f-9ecb-c16298769a21">IDvbLogicalChannel2Descriptor::GetCountOfLists</a>
  method to get the number of channel lists in the logical channel descriptor.


### -param pbVal [out]

Receives the number of channels in the list.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc60db7f-ae49-48dd-bd8a-62899e5ca7a3">IDvbLogicalChannel2Descriptor</a>



<a href="https://msdn.microsoft.com/97cadf6c-2549-4a7f-9ecb-c16298769a21">IDvbLogicalChannel2Descriptor::GetCountOfLists</a>
 

 


---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListNameW
title: IDvbLogicalChannel2Descriptor::GetListNameW method
author: windows-driver-content
description: Gets the name of a channel list from a Digital Video Broadcast (DVB) logical channel descriptor.
old-location: mstv\idvblogicalchannel2descriptor_getlistnamew.htm
old-project: mstv
ms.assetid: cbfee1d5-8a38-4c9a-ae5e-2d91970c132e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetListNameW method [Microsoft TV Technologies], GetListNameW method [Microsoft TV Technologies], IDvbLogicalChannel2Descriptor interface, GetListNameW,IDvbLogicalChannel2Descriptor.GetListNameW, IDvbLogicalChannel2Descriptor, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies], GetListNameW method, IDvbLogicalChannel2Descriptor::GetListNameW, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListNameW, mstv.idvblogicalchannel2descriptor_getlistnamew
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbLogicalChannel2Descriptor.GetListNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLogicalChannel2Descriptor::GetListNameW method


## -description


Gets the name of a channel list from a Digital Video Broadcast (DVB) logical channel descriptor.


## -parameters




### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>
  method to get the number of channel list records in the logical channel descriptor.


### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to the memory block that receives the channel name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc60db7f-ae49-48dd-bd8a-62899e5ca7a3">IDvbLogicalChannel2Descriptor</a>



<a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>
 

 


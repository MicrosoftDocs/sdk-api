---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListCountryCode
title: IDvbLogicalChannel2Descriptor::GetListCountryCode
author: windows-driver-content
description: Gets the three-character ISO 3166 country code for a channel list in a Digital Video Broadcast (DVB) logical channel descriptor.
old-location: mstv\idvblogicalchannel2descriptor_getlistcountrycode.htm
old-project: mstv
ms.assetid: 42f3c684-64c3-4bcb-b9c0-25a008075902
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetListCountryCode, GetListCountryCode method [Microsoft TV Technologies], GetListCountryCode method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListCountryCode method, IDvbLogicalChannel2Descriptor.GetListCountryCode, IDvbLogicalChannel2Descriptor::GetListCountryCode, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountryCode, mstv.idvblogicalchannel2descriptor_getlistcountrycode
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
-	IDvbLogicalChannel2Descriptor.GetListCountryCode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbLogicalChannel2Descriptor::GetListCountryCode


## -description


Gets the three-character ISO 3166 country code for a channel list in a  Digital Video Broadcast (DVB) logical channel descriptor.


## -parameters




### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>
  method to get the number of channel list records in the logical channel descriptor.


### -param pszCode [out]

Pointer to a buffer that receives the country code. This code is a 3-character, null-terminated string, so the buffer must be at least four bytes long. The caller is responsible for releasing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc60db7f-ae49-48dd-bd8a-62899e5ca7a3">IDvbLogicalChannel2Descriptor</a>
 

 


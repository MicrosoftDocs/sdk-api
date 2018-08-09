---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetRecordItemRawBytes
title: IDvbExtendedEventDescriptor::GetRecordItemRawBytes
author: windows-sdk-content
description: Gets the raw data from the current item in a Digital Video Broadcast (DVB) extended event descriptor.
old-location: mstv\idvbextendedeventdescriptor_getrecorditemrawbytes.htm
old-project: mstv
ms.assetid: ed3046ad-b987-479a-a2ba-d761b2d83c86
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordItemRawBytes, GetRecordItemRawBytes method [Microsoft TV Technologies], GetRecordItemRawBytes method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetRecordItemRawBytes method, IDvbExtendedEventDescriptor.GetRecordItemRawBytes, IDvbExtendedEventDescriptor::GetRecordItemRawBytes, dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemRawBytes, mstv.idvbextendedeventdescriptor_getrecorditemrawbytes
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
 - IDvbExtendedEventDescriptor.GetRecordItemRawBytes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbExtendedEventDescriptor::GetRecordItemRawBytes


## -description


Gets the raw data from the 
current item in a Digital Video Broadcast (DVB) extended event descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the item record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/db065f1a-8354-4207-b7f7-d67adf094c70">IDvbExtendedEventDescriptor::GetCountOfRecords</a>method to get the number of records in the extended event descriptor.


### -param ppbRawItem [out]

Pointer to a buffer that gets the item data. The caller is responsible for freeing this memory.


### -param pbItemLength [out]

Receives the number of bytes in the item description.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/db100f17-f7b8-4252-8090-44567ab9dcbe">IDvbExtendedEventDescriptor</a>



<a href="https://msdn.microsoft.com/db065f1a-8354-4207-b7f7-d67adf094c70">IDvbExtendedEventDescriptor::GetCountOfRecords</a>
 

 


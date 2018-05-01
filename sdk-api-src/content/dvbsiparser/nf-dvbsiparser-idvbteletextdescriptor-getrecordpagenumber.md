---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetRecordPageNumber
title: IDvbTeletextDescriptor::GetRecordPageNumber method
author: windows-driver-content
description: Gets the page number a Digital Video Broadcast (DVB) teletext descriptor. The page number identifies the page of teletext that is broadcast.
old-location: mstv\idvbteletextdescriptor_getrecordpagenumber.htm
old-project: mstv
ms.assetid: 323af443-8ef3-443e-9d6c-7af17419655a
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordPageNumber method [Microsoft TV Technologies], GetRecordPageNumber method [Microsoft TV Technologies], IDvbTeletextDescriptor interface, GetRecordPageNumber,IDvbTeletextDescriptor.GetRecordPageNumber, IDvbTeletextDescriptor, IDvbTeletextDescriptor interface [Microsoft TV Technologies], GetRecordPageNumber method, IDvbTeletextDescriptor::GetRecordPageNumber, dvbsiparser/IDvbTeletextDescriptor::GetRecordPageNumber, mstv.idvbteletextdescriptor_getrecordpagenumber
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbTeletextDescriptor.GetRecordPageNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbTeletextDescriptor::GetRecordPageNumber method


## -description



  Gets the page number a Digital Video Broadcast (DVB) teletext descriptor.  The page number identifies the page of teletext that is broadcast.



## -parameters




### -param bRecordIndex [in]


  Zero-based index of the descriptor to return. To get the number of descriptors, 
  call <a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">IDvbTeletextDescriptor::GetCountOfRecords</a>



### -param pbVal [out]

Receives the page number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5148a87b-e6b6-4bda-871c-10a2f398ebcc">IDvbTeletextDescriptor</a>



<a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">IDvbTeletextDescriptor::GetCountOfRecords</a>
 

 


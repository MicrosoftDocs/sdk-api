---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetRecordMagazineNumber
title: IDvbTeletextDescriptor::GetRecordMagazineNumber
author: windows-sdk-content
description: Gets the magazine number from a Digital Video Broadcast (DVB) teletext descriptor.
old-location: mstv\idvbteletextdescriptor_getrecordmagazinenumber.htm
old-project: mstv
ms.assetid: bb3c39b6-dc85-42ca-9d4b-ad27eae077dd
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordMagazineNumber, GetRecordMagazineNumber method [Microsoft TV Technologies], GetRecordMagazineNumber method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetRecordMagazineNumber method, IDvbTeletextDescriptor.GetRecordMagazineNumber, IDvbTeletextDescriptor::GetRecordMagazineNumber, dvbsiparser/IDvbTeletextDescriptor::GetRecordMagazineNumber, mstv.idvbteletextdescriptor_getrecordmagazinenumber
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
 - IDvbTeletextDescriptor.GetRecordMagazineNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbTeletextDescriptor::GetRecordMagazineNumber


## -description


Gets the magazine number from a Digital Video Broadcast (DVB) teletext descriptor.
  A <i>magazine</i> is a sequence of one or more pages in an enhanced-teletext packet that are normally repeatedly transmitted in numerical sequence


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call 
  <a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">IDvbTeletextDescriptor::GetCountOfRecords
</a>.



### -param pbVal [out]

Receives the magazine number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5148a87b-e6b6-4bda-871c-10a2f398ebcc">IDvbTeletextDescriptor</a>



<a href="https://msdn.microsoft.com/a802c685-9d7a-446a-a29c-4fc3e9ad3dc4">IDvbTeletextDescriptor::GetCountOfRecords
</a>
 

 


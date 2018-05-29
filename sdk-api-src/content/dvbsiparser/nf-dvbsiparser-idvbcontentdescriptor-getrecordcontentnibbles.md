---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetRecordContentNibbles
title: IDvbContentDescriptor::GetRecordContentNibbles
author: windows-sdk-content
description: Gets the two 4-bit fields that make up a DVB-defined identifier for a content descriptor.
old-location: mstv\idvbcontentdescriptor_getrecordcontentnibbles.htm
old-project: mstv
ms.assetid: 2b05403a-cf9e-4f23-907f-ffb90b6fc5e3
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetRecordContentNibbles, GetRecordContentNibbles method [Microsoft TV Technologies], GetRecordContentNibbles method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetRecordContentNibbles method, IDvbContentDescriptor.GetRecordContentNibbles, IDvbContentDescriptor::GetRecordContentNibbles, dvbsiparser/IDvbContentDescriptor::GetRecordContentNibbles, mstv.idvbcontentdescriptor_getrecordcontentnibbles
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbContentDescriptor.GetRecordContentNibbles
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbContentDescriptor::GetRecordContentNibbles


## -description


Gets the two 4-bit fields that make up a DVB-defined identifier for a content descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/0d4d81b3-d6d8-416b-af6b-2b6ef12cf1d9">IDvbContentDescriptor::GetCountOfRecords</a>



### -param pbValLevel1 [out]

Gets the most-significant four bits of the content identifier.


### -param pbValLevel2 [out]

Gets the least-significant four bits of the content identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For a list of content descriptors associated with the values returned in the <i>dwVal1</i> and <i>dwVal2</i> parameters, see Table 28 in Section 6.2.9 of the DVB standard document titled  
      <i>Digital Video Broadcasting (DVB);
Specification for Service Information (SI) in DVB systems (DVB Document A038 Rev. 4)</i>. (This resource may not be available in some languages 

and countries.)




## -see-also




<a href="https://msdn.microsoft.com/7bc74428-f8e3-4d3b-b35a-33e917b18a93">IDvbContentDescriptor</a>
 

 


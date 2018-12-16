---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetRecordUserNibbles
title: IDvbContentDescriptor::GetRecordUserNibbles
author: windows-sdk-content
description: Gets the two 4-bit fields that make up a broadcaster-defined identifier for a content descriptor.
old-location: mstv\idvbcontentdescriptor_getrecordusernibbles.htm
tech.root: mstv
ms.assetid: a071e725-c98d-4061-bda5-d7eca8b4b0e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetRecordUserNibbles, GetRecordUserNibbles method [Microsoft TV Technologies], GetRecordUserNibbles method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetRecordUserNibbles method, IDvbContentDescriptor.GetRecordUserNibbles, IDvbContentDescriptor::GetRecordUserNibbles, dvbsiparser/IDvbContentDescriptor::GetRecordUserNibbles, mstv.idvbcontentdescriptor_getrecordusernibbles
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
 - IDvbContentDescriptor.GetRecordUserNibbles
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbContentDescriptor::GetRecordUserNibbles


## -description


Gets the two 4-bit fields that make up a broadcaster-defined identifier for a content descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/0d4d81b3-d6d8-416b-af6b-2b6ef12cf1d9">IDvbContentDescriptor::GetCountOfRecords</a>



### -param pbVal1 [out]

Gets the most-significant four bits of the broadcaster-defined content identifier. These bits are returned in the  right-most four bits of the byte. 


### -param pbVal2 [out]

Gets the least-significant four bits of the broadcaster-defined  content identifier. These bits are returned in the left-most four bits of the byte.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7bc74428-f8e3-4d3b-b35a-33e917b18a93">IDvbContentDescriptor</a>
 

 


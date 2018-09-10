---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetRecordAncillaryPageID
title: IDvbSubtitlingDescriptor::GetRecordAncillaryPageID
author: windows-sdk-content
description: Gets the ancillary page identifier for a Digital Video Broadcast (DVB) subtitling descriptor.
old-location: mstv\idvbsubtitlingdescriptor_getrecordancillarypageid.htm
tech.root: mstv
ms.assetid: ab490087-063d-4e9f-8aa5-679804548d26
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordAncillaryPageID, GetRecordAncillaryPageID method [Microsoft TV Technologies], GetRecordAncillaryPageID method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetRecordAncillaryPageID method, IDvbSubtitlingDescriptor.GetRecordAncillaryPageID, IDvbSubtitlingDescriptor::GetRecordAncillaryPageID, dvbsiparser/IDvbSubtitlingDescriptor::GetRecordAncillaryPageID, mstv.idvbsubtitlingdescriptor_getrecordancillarypageid
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
 - IDvbSubtitlingDescriptor.GetRecordAncillaryPageID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvbSubtitlingDescriptor::GetRecordAncillaryPageID


## -description


 Gets the ancillary page identifier for a Digital Video Broadcast (DVB) subtitling descriptor.  The DVB subtitling segments signalling the ancillary page identifier are decoded if the previous data in the subtitling descriptor matches the user's selection criteria. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/8cc25b63-de43-4f8d-af19-c3bb8c389a55">IDvbSubtitlingDescriptor::GetCountOfRecords</a>



### -param pwVal [out]

Receives the ancillary page identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the subtitling descriptor has no ancillary page, the values in
the ancillary_page_id and composition_page_id fields of the descriptor are the same.

 The ancillary_page_id is never signalled in a composition segment. It may be signalled in color
lookup table (CLUT) definition segments, object segments, or any other type of segment.




## -see-also




<a href="https://msdn.microsoft.com/7308e8a9-6e16-4719-b87e-9445499f499c">IDvbSubtitlingDescriptor</a>



<a href="https://msdn.microsoft.com/8cc25b63-de43-4f8d-af19-c3bb8c389a55">IDvbSubtitlingDescriptor::GetCountOfRecords</a>
 

 


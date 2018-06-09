---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetRecordCompositionPageID
title: IDvbSubtitlingDescriptor::GetRecordCompositionPageID
author: windows-sdk-content
description: Gets the composition page identifier for a Digital Video Broadcast (DVB) subtitling descriptor.
old-location: mstv\idvbsubtitlingdescriptor_getrecordcompositionpageid.htm
old-project: mstv
ms.assetid: 108f431a-e3c3-42d5-ad27-b7a54029051f
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordCompositionPageID, GetRecordCompositionPageID method [Microsoft TV Technologies], GetRecordCompositionPageID method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetRecordCompositionPageID method, IDvbSubtitlingDescriptor.GetRecordCompositionPageID, IDvbSubtitlingDescriptor::GetRecordCompositionPageID, dvbsiparser/IDvbSubtitlingDescriptor::GetRecordCompositionPageID, mstv.idvbsubtitlingdescriptor_getrecordcompositionpageid
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
 - IDvbSubtitlingDescriptor.GetRecordCompositionPageID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbSubtitlingDescriptor::GetRecordCompositionPageID


## -description


 Gets the composition page identifier for a Digital Video Broadcast (DVB) subtitling descriptor. DVB subtitling segments that signal a
composition page identifier are decoded if the previous data in the subtitling descriptor matches the user's selection criteria.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/8cc25b63-de43-4f8d-af19-c3bb8c389a55">IDvbSubtitlingDescriptor::GetCountOfRecords</a>



### -param pwVal [out]

Receives the composition page identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The composition page identifier is signalled in at least the subtitling segments that define the data
structure of the subtitle screen: the page composition segment and region composition segments. It
may additionally be signalled in segments containing data on which the composition depends.




## -see-also




<a href="https://msdn.microsoft.com/7308e8a9-6e16-4719-b87e-9445499f499c">IDvbSubtitlingDescriptor</a>



<a href="https://msdn.microsoft.com/8cc25b63-de43-4f8d-af19-c3bb8c389a55">IDvbSubtitlingDescriptor::GetCountOfRecords</a>
 

 


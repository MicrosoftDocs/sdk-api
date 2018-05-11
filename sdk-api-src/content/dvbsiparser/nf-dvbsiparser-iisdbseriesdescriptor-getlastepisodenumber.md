---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetLastEpisodeNumber
title: IIsdbSeriesDescriptor::GetLastEpisodeNumber
author: windows-driver-content
description: Gets the number of the last episode of a series from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
old-location: mstv\iisdbseriesdescriptor_getlastepisodenumber.htm
old-project: mstv
ms.assetid: 23cae82f-a40f-47c6-b9ee-0d91a87d9b70
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetLastEpisodeNumber, GetLastEpisodeNumber method [Microsoft TV Technologies], GetLastEpisodeNumber method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetLastEpisodeNumber method, IIsdbSeriesDescriptor.GetLastEpisodeNumber, IIsdbSeriesDescriptor::GetLastEpisodeNumber, dvbsiparser/IIsdbSeriesDescriptor::GetLastEpisodeNumber, mstv.iisdbseriesdescriptor_getlastepisodenumber
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
-	IIsdbSeriesDescriptor.GetLastEpisodeNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSeriesDescriptor::GetLastEpisodeNumber


## -description


Gets the number of the last episode of a series from an Integrated Services Digital Broadcasting (ISDB) series descriptor.


## -parameters




### -param pwVal [out]

Receives the last episode number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07c4debc-1817-46ac-9f67-9b8637a04662">IIsdbSeriesDescriptor</a>
 

 


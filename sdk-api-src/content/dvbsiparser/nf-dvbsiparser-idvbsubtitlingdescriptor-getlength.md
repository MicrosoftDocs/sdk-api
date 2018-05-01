---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetLength
title: IDvbSubtitlingDescriptor::GetLength method
author: windows-driver-content
description: Gets the body length of a Digital Video Broadcast (DVB) subtitling descriptor.
old-location: mstv\idvbsubtitlingdescriptor_getlength.htm
old-project: mstv
ms.assetid: 1b02c37c-4411-4d69-af5d-d758b18fe42c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies], IDvbSubtitlingDescriptor interface, GetLength,IDvbSubtitlingDescriptor.GetLength, IDvbSubtitlingDescriptor, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies], GetLength method, IDvbSubtitlingDescriptor::GetLength, dvbsiparser/IDvbSubtitlingDescriptor::GetLength, mstv.idvbsubtitlingdescriptor_getlength
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
-	IDvbSubtitlingDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbSubtitlingDescriptor::GetLength method


## -description


Gets the body length of a Digital Video Broadcast (DVB) subtitling descriptor. 


## -parameters




### -param pbVal [out]

Receives the number of bytes in the descriptor.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7308e8a9-6e16-4719-b87e-9445499f499c">IDvbSubtitlingDescriptor</a>
 

 


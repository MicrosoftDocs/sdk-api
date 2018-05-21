---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetLength
title: IDvbTeletextDescriptor::GetLength
author: windows-driver-content
description: Gets the body length of a Digital Video Broadcast (DVB) teletext descriptor.
old-location: mstv\idvbteletextdescriptor_getlength.htm
old-project: mstv
ms.assetid: e785d05a-d4f1-40d8-b93e-ea944373f4c3
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbTeletextDescriptor.GetLength, IDvbTeletextDescriptor::GetLength, dvbsiparser/IDvbTeletextDescriptor::GetLength, mstv.idvbteletextdescriptor_getlength
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
-	IDvbTeletextDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbTeletextDescriptor::GetLength


## -description



  Gets the body length of a Digital Video Broadcast (DVB) teletext descriptor.
  


## -parameters




### -param pbVal [out]

Receives the length of the teletext descriptor, in bytes.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5148a87b-e6b6-4bda-871c-10a2f398ebcc">IDvbTeletextDescriptor</a>
 

 


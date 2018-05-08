---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetLength
title: IIsdbDataContentDescriptor::GetLength
author: windows-driver-content
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes.
old-location: mstv\iisdbdatacontentdescriptor_getlength.htm
old-project: mstv
ms.assetid: 51546c62-5042-460d-a792-2253bd57df13
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbDataContentDescriptor.GetLength, IIsdbDataContentDescriptor::GetLength, dvbsiparser/IIsdbDataContentDescriptor::GetLength, mstv.iisdbdatacontentdescriptor_getlength
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
-	IIsdbDataContentDescriptor.GetLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDataContentDescriptor::GetLength


## -description


 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes. 


## -parameters




### -param pbVal [out]

Receives the descriptor length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 


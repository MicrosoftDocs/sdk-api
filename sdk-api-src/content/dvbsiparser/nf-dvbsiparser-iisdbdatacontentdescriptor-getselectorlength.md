---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetSelectorLength
title: IIsdbDataContentDescriptor::GetSelectorLength method
author: windows-driver-content
description: Gets the length of the selector part of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes.
old-location: mstv\iisdbdatacontentdescriptor_getselectorlength.htm
old-project: mstv
ms.assetid: 485ac963-e85a-41cc-adcd-93590b327061
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetSelectorLength method [Microsoft TV Technologies], GetSelectorLength method [Microsoft TV Technologies], IIsdbDataContentDescriptor interface, GetSelectorLength,IIsdbDataContentDescriptor.GetSelectorLength, IIsdbDataContentDescriptor, IIsdbDataContentDescriptor interface [Microsoft TV Technologies], GetSelectorLength method, IIsdbDataContentDescriptor::GetSelectorLength, dvbsiparser/IIsdbDataContentDescriptor::GetSelectorLength, mstv.iisdbdatacontentdescriptor_getselectorlength
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
-	IIsdbDataContentDescriptor.GetSelectorLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDataContentDescriptor::GetSelectorLength method


## -description


Gets the length of the selector part of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes.


## -parameters




### -param pbVal [out]

Receives the selector length.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 


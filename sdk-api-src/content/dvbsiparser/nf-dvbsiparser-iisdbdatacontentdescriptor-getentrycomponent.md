---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetEntryComponent
title: IIsdbDataContentDescriptor::GetEntryComponent
author: windows-driver-content
description: Gets the value of the entry_component field from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field indicates the first component stream that is referenced in the descriptor.
old-location: mstv\iisdbdatacontentdescriptor_getentrycomponent.htm
old-project: mstv
ms.assetid: 9f8f9e55-cc03-4f07-918e-19199485c8d4
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetEntryComponent, GetEntryComponent method [Microsoft TV Technologies], GetEntryComponent method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetEntryComponent method, IIsdbDataContentDescriptor.GetEntryComponent, IIsdbDataContentDescriptor::GetEntryComponent, dvbsiparser/IIsdbDataContentDescriptor::GetEntryComponent, mstv.iisdbdatacontentdescriptor_getentrycomponent
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
-	IIsdbDataContentDescriptor.GetEntryComponent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDataContentDescriptor::GetEntryComponent


## -description


 Gets the value of the entry_component field from an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field indicates the first component stream that is referenced in the descriptor.


## -parameters




### -param pbVal [out]

Returns the entry_component field value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 


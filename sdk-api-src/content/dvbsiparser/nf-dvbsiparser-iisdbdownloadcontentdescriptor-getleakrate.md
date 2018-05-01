---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetLeakRate
title: IIsdbDownloadContentDescriptor::GetLeakRate method
author: windows-driver-content
description: Gets the leak rate of the transport buffer from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes per second.
old-location: mstv\iisdbdownloadcontentdescriptor_getleakrate.htm
old-project: mstv
ms.assetid: 3e85f026-66bf-4c13-b476-3aca9e28b3b6
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetLeakRate method [Microsoft TV Technologies], GetLeakRate method [Microsoft TV Technologies], IIsdbDownloadContentDescriptor interface, GetLeakRate,IIsdbDownloadContentDescriptor.GetLeakRate, IIsdbDownloadContentDescriptor, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies], GetLeakRate method, IIsdbDownloadContentDescriptor::GetLeakRate, dvbsiparser/IIsdbDownloadContentDescriptor::GetLeakRate, mstv.iisdbdownloadcontentdescriptor_getleakrate
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
-	IIsdbDownloadContentDescriptor.GetLeakRate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDownloadContentDescriptor::GetLeakRate method


## -description


 Gets the leak rate of the transport buffer from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes per second.


## -parameters




### -param pdwVal [out]

Receives the leak rate.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>
 

 


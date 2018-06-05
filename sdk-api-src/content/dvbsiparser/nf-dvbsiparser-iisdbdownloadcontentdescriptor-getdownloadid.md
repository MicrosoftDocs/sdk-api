---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetDownloadId
title: IIsdbDownloadContentDescriptor::GetDownloadId
author: windows-sdk-content
description: Gets the download identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The download identifier identifies an application number for the download.
old-location: mstv\iisdbdownloadcontentdescriptor_getdownloadid.htm
old-project: mstv
ms.assetid: b57eba56-b9d6-4555-8d5d-80fd2b9fd23f
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetDownloadId, GetDownloadId method [Microsoft TV Technologies], GetDownloadId method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetDownloadId method, IIsdbDownloadContentDescriptor.GetDownloadId, IIsdbDownloadContentDescriptor::GetDownloadId, dvbsiparser/IIsdbDownloadContentDescriptor::GetDownloadId, mstv.iisdbdownloadcontentdescriptor_getdownloadid
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbDownloadContentDescriptor.GetDownloadId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDownloadContentDescriptor::GetDownloadId


## -description


 Gets the download identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The download identifier identifies an application number for the download.


## -parameters




### -param pdwVal [out]

Receives the download identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>
 

 


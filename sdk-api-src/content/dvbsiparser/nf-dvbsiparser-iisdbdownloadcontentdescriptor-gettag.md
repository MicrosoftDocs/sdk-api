---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetTag
title: IIsdbDownloadContentDescriptor::GetTag method
author: windows-driver-content
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
old-location: mstv\iisdbdownloadcontentdescriptor_gettag.htm
old-project: mstv
ms.assetid: a78c3f3b-aaa2-4b5e-9cf8-7746f20fafc2
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies], IIsdbDownloadContentDescriptor interface, GetTag,IIsdbDownloadContentDescriptor.GetTag, IIsdbDownloadContentDescriptor, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies], GetTag method, IIsdbDownloadContentDescriptor::GetTag, dvbsiparser/IIsdbDownloadContentDescriptor::GetTag, mstv.iisdbdownloadcontentdescriptor_gettag
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
-	IIsdbDownloadContentDescriptor.GetTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDownloadContentDescriptor::GetTag method


## -description


Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) download content descriptor.


## -parameters




### -param pbVal [out]

Receives the tag value. For ISDB download content descriptors, this value is 0xC9.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>
 

 


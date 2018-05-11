---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetComponentSize
title: IIsdbDownloadContentDescriptor::GetComponentSize
author: windows-driver-content
description: Gets the total size of components transmitted within the same carousel from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.
old-location: mstv\iisdbdownloadcontentdescriptor_getcomponentsize.htm
old-project: mstv
ms.assetid: 07edb403-6674-4673-928c-91e7df9fe9da
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetComponentSize, GetComponentSize method [Microsoft TV Technologies], GetComponentSize method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetComponentSize method, IIsdbDownloadContentDescriptor.GetComponentSize, IIsdbDownloadContentDescriptor::GetComponentSize, dvbsiparser/IIsdbDownloadContentDescriptor::GetComponentSize, mstv.iisdbdownloadcontentdescriptor_getcomponentsize
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
-	IIsdbDownloadContentDescriptor.GetComponentSize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDownloadContentDescriptor::GetComponentSize


## -description


Gets the total size of components transmitted within the same carousel from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.


## -parameters




### -param pdwVal [out]

Receives the component size.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>
 

 


---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetLeakRate
title: IIsdbDownloadContentDescriptor::GetLeakRate (dvbsiparser.h)
author: windows-sdk-content
description: Gets the leak rate of the transport buffer from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes per second.
old-location: mstv\iisdbdownloadcontentdescriptor_getleakrate.htm
tech.root: mstv
ms.assetid: 3e85f026-66bf-4c13-b476-3aca9e28b3b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLeakRate, GetLeakRate method [Microsoft TV Technologies], GetLeakRate method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetLeakRate method, IIsdbDownloadContentDescriptor.GetLeakRate, IIsdbDownloadContentDescriptor::GetLeakRate, dvbsiparser/IIsdbDownloadContentDescriptor::GetLeakRate, mstv.iisdbdownloadcontentdescriptor_getleakrate
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbDownloadContentDescriptor.GetLeakRate"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbDownloadContentDescriptor.GetLeakRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbDownloadContentDescriptor::GetLeakRate


## -description


 Gets the leak rate of the transport buffer from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes per second.


## -parameters




### -param pdwVal [out]

Receives the leak rate.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>
 

 


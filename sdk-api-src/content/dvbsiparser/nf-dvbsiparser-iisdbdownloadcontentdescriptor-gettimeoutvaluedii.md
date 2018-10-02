---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetTimeOutValueDII
title: IIsdbDownloadContentDescriptor::GetTimeOutValueDII
author: windows-sdk-content
description: Gets the value of the time_out_value_DII field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
old-location: mstv\iisdbdownloadcontentdescriptor_gettimeoutvaluedii.htm
tech.root: MSTV
ms.assetid: ec1bd153-e637-4046-8d7b-f2868c4909dd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetTimeOutValueDII, GetTimeOutValueDII method [Microsoft TV Technologies], GetTimeOutValueDII method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetTimeOutValueDII method, IIsdbDownloadContentDescriptor.GetTimeOutValueDII, IIsdbDownloadContentDescriptor::GetTimeOutValueDII, dvbsiparser/IIsdbDownloadContentDescriptor::GetTimeOutValueDII, mstv.iisdbdownloadcontentdescriptor_gettimeoutvaluedii
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
 - IIsdbDownloadContentDescriptor.GetTimeOutValueDII
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDownloadContentDescriptor::GetTimeOutValueDII


## -description


 Gets the  value of the time_out_value_DII field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The time_out_value_DII field indicates the recommended timeout value  for receiving all sections of the corresponding carousel, in milliseconds.


## -parameters




### -param pdwVal [out]

Receives the recommended timeout value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>
 

 


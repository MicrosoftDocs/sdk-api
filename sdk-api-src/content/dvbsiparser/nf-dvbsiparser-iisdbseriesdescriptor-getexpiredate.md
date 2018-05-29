---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetExpireDate
title: IIsdbSeriesDescriptor::GetExpireDate
author: windows-sdk-content
description: Gets a series expiration date from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
old-location: mstv\iisdbseriesdescriptor_getexpiredate.htm
old-project: mstv
ms.assetid: 0d658904-4f81-443b-b69d-814e606dabc4
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetExpireDate, GetExpireDate method [Microsoft TV Technologies], GetExpireDate method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetExpireDate method, IIsdbSeriesDescriptor.GetExpireDate, IIsdbSeriesDescriptor::GetExpireDate, dvbsiparser/IIsdbSeriesDescriptor::GetExpireDate, mstv.iisdbseriesdescriptor_getexpiredate
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbSeriesDescriptor.GetExpireDate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSeriesDescriptor::GetExpireDate


## -description


Gets a series expiration date from an Integrated Services Digital Broadcasting (ISDB) series descriptor.


## -parameters




### -param pfValid [out]

Receives a flag that indicates whether the series expiration date in the descriptor expire_date field is valid.


### -param pmdtVal [out]

Receives the date and time when the series expires.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07c4debc-1817-46ac-9f67-9b8637a04662">IIsdbSeriesDescriptor</a>
 

 


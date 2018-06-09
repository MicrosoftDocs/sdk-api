---
UID: NF:dvbsiparser.IISDB_SDTT.GetServiceId
title: IISDB_SDTT::GetServiceId
author: windows-sdk-content
description: Receives the service_id field that uniquely identifies a service from an Integrated Services Digital Broadcasting System (ISDB) software download trigger table (SDTT).
old-location: mstv\iisdb_sdtt_getserviceid.htm
old-project: mstv
ms.assetid: 36e9d2b7-f89a-47ad-9fd2-d9aa8d76949c
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetServiceId, GetServiceId method [Microsoft TV Technologies], GetServiceId method [Microsoft TV Technologies],IISDB_SDTT interface, IISDB_SDTT interface [Microsoft TV Technologies],GetServiceId method, IISDB_SDTT.GetServiceId, IISDB_SDTT::GetServiceId, dvbsiparser/IISDB_SDTT::GetServiceId, mstv.iisdb_sdtt_getserviceid
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_SDTT.GetServiceId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_SDTT::GetServiceId


## -description



  Receives the service_id field that uniquely identifies a service from
  an Integrated Services Digital Broadcasting System
  (ISDB)  software download
  trigger table
  (SDTT). 


## -parameters




### -param pwVal [out]

Receives the service_id value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f6ed35bc-4470-4000-8f0d-19d454453720">IISDB_SDTT</a>
 

 


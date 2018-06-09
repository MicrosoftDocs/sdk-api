---
UID: NF:dvbsiparser.IISDB_CDT.GetDownloadDataId
title: IISDB_CDT::GetDownloadDataId
author: windows-sdk-content
description: Receives the download_data_id field value for a logo transmission descriptor from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT). The download_data_id field identifies the data to be downloaded.
old-location: mstv\iisdb_cdt_getdownloaddataid.htm
old-project: mstv
ms.assetid: 87cd757e-ed10-4ad2-a9d5-4a92b8d48cd2
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetDownloadDataId, GetDownloadDataId method [Microsoft TV Technologies], GetDownloadDataId method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetDownloadDataId method, IISDB_CDT.GetDownloadDataId, IISDB_CDT::GetDownloadDataId, dvbsiparser/IISDB_CDT::GetDownloadDataId, mstv.iisdb_cdt_getdownloaddataid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IISDB_CDT.GetDownloadDataId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_CDT::GetDownloadDataId


## -description



  Receives the download_data_id field value 
  for a logo transmission descriptor from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
  The download_data_id field identifies the data to be downloaded.


## -parameters




### -param pwVal [out]

Receives the download_data_id field value. This value is the same as the value of the table_id_extension field for the CDT containing the logo data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>
 

 


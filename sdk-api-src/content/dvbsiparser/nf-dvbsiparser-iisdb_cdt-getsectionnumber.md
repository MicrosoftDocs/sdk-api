---
UID: NF:dvbsiparser.IISDB_CDT.GetSectionNumber
title: IISDB_CDT::GetSectionNumber method
author: windows-driver-content
description: Gets the section_number field value from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
old-location: mstv\iisdb_cdt_getsectionnumber.htm
old-project: mstv
ms.assetid: 61825be5-01c4-4d5f-be4a-6752ebf8dee8
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetSectionNumber method [Microsoft TV Technologies], GetSectionNumber method [Microsoft TV Technologies], IISDB_CDT interface, GetSectionNumber,IISDB_CDT.GetSectionNumber, IISDB_CDT, IISDB_CDT interface [Microsoft TV Technologies], GetSectionNumber method, IISDB_CDT::GetSectionNumber, dvbsiparser/IISDB_CDT::GetSectionNumber, mstv.iisdb_cdt_getsectionnumber
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IISDB_CDT.GetSectionNumber
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IISDB_CDT::GetSectionNumber method


## -description



  Gets the section_number field value from
  an Integrated Services Digital Broadcasting
  (ISDB)
  common data table (CDT). The section_number field identifies the position of a subtable within the CDT so that the CDT can be reassembled with its subtables in the proper order.


## -parameters




### -param pbVal [out]

Receives the section_number field value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6e0ceabb-4d67-46c1-9e7d-e00d5ad82280">IISDB_CDT</a>
 

 


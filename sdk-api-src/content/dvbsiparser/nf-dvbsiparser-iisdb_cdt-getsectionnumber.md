---
UID: NF:dvbsiparser.IISDB_CDT.GetSectionNumber
title: IISDB_CDT::GetSectionNumber (dvbsiparser.h)
description: Gets the section_number field value from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
helpviewer_keywords: ["GetSectionNumber","GetSectionNumber method [Microsoft TV Technologies]","GetSectionNumber method [Microsoft TV Technologies]","IISDB_CDT interface","IISDB_CDT interface [Microsoft TV Technologies]","GetSectionNumber method","IISDB_CDT.GetSectionNumber","IISDB_CDT::GetSectionNumber","dvbsiparser/IISDB_CDT::GetSectionNumber","mstv.iisdb_cdt_getsectionnumber"]
old-location: mstv\iisdb_cdt_getsectionnumber.htm
tech.root: mstv
ms.assetid: 61825be5-01c4-4d5f-be4a-6752ebf8dee8
ms.date: 12/05/2018
ms.keywords: GetSectionNumber, GetSectionNumber method [Microsoft TV Technologies], GetSectionNumber method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetSectionNumber method, IISDB_CDT.GetSectionNumber, IISDB_CDT::GetSectionNumber, dvbsiparser/IISDB_CDT::GetSectionNumber, mstv.iisdb_cdt_getsectionnumber
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IISDB_CDT::GetSectionNumber
 - dvbsiparser/IISDB_CDT::GetSectionNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_CDT.GetSectionNumber
---

# IISDB_CDT::GetSectionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the section_number field value from
  an Integrated Services Digital Broadcasting
  (ISDB)
  common data table (CDT). The section_number field identifies the position of a subtable within the CDT so that the CDT can be reassembled with its subtables in the proper order.

## -parameters

### -param pbVal [out]

Receives the section_number field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>
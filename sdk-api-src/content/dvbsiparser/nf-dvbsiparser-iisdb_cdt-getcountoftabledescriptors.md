---
UID: NF:dvbsiparser.IISDB_CDT.GetCountOfTableDescriptors
title: IISDB_CDT::GetCountOfTableDescriptors (dvbsiparser.h)
description: Returns the number of descriptors for logos in an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
helpviewer_keywords: ["GetCountOfTableDescriptors","GetCountOfTableDescriptors method [Microsoft TV Technologies]","GetCountOfTableDescriptors method [Microsoft TV Technologies]","IISDB_CDT interface","IISDB_CDT interface [Microsoft TV Technologies]","GetCountOfTableDescriptors method","IISDB_CDT.GetCountOfTableDescriptors","IISDB_CDT::GetCountOfTableDescriptors","dvbsiparser/IISDB_CDT::GetCountOfTableDescriptors","mstv.iisdb_cdt_getcountoftabledescriptors"]
old-location: mstv\iisdb_cdt_getcountoftabledescriptors.htm
tech.root: mstv
ms.assetid: ea01a53f-8d0b-4594-87b4-d293901fca19
ms.date: 12/05/2018
ms.keywords: GetCountOfTableDescriptors, GetCountOfTableDescriptors method [Microsoft TV Technologies], GetCountOfTableDescriptors method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetCountOfTableDescriptors method, IISDB_CDT.GetCountOfTableDescriptors, IISDB_CDT::GetCountOfTableDescriptors, dvbsiparser/IISDB_CDT::GetCountOfTableDescriptors, mstv.iisdb_cdt_getcountoftabledescriptors
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
 - IISDB_CDT::GetCountOfTableDescriptors
 - dvbsiparser/IISDB_CDT::GetCountOfTableDescriptors
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
 - IISDB_CDT.GetCountOfTableDescriptors
---

# IISDB_CDT::GetCountOfTableDescriptors


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns the number of descriptors for logos in
  an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).

## -parameters

### -param pdwVal [out]

Receives the count of logo descriptors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>
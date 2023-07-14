---
UID: NF:dvbsiparser.IISDB_CDT.GetTableDescriptorByIndex
title: IISDB_CDT::GetTableDescriptorByIndex (dvbsiparser.h)
description: Returns a specified logo transmission descriptor from an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
helpviewer_keywords: ["GetTableDescriptorByIndex","GetTableDescriptorByIndex method [Microsoft TV Technologies]","GetTableDescriptorByIndex method [Microsoft TV Technologies]","IISDB_CDT interface","IISDB_CDT interface [Microsoft TV Technologies]","GetTableDescriptorByIndex method","IISDB_CDT.GetTableDescriptorByIndex","IISDB_CDT::GetTableDescriptorByIndex","dvbsiparser/IISDB_CDT::GetTableDescriptorByIndex","mstv.iisdb_cdt_gettabledescriptorbyindex"]
old-location: mstv\iisdb_cdt_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: e345e860-247a-4c30-876b-c0e6c82767b8
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IISDB_CDT.GetTableDescriptorByIndex, IISDB_CDT::GetTableDescriptorByIndex, dvbsiparser/IISDB_CDT::GetTableDescriptorByIndex, mstv.iisdb_cdt_gettabledescriptorbyindex
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
 - IISDB_CDT::GetTableDescriptorByIndex
 - dvbsiparser/IISDB_CDT::GetTableDescriptorByIndex
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
 - IISDB_CDT.GetTableDescriptorByIndex
---

# IISDB_CDT::GetTableDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Returns a specified logo transmission descriptor
  from an Integrated Services Digital Broadcasting (ISDB) 
  common data table (CDT).

## -parameters

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdb_cdt-getcountoftabledescriptors">IISDB_CDT::GetCountOfTableDescriptors</a> method to get the number of table descriptors.

### -param ppDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface implemented by the descriptor. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>
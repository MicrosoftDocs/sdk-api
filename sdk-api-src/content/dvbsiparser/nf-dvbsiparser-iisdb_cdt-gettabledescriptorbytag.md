---
UID: NF:dvbsiparser.IISDB_CDT.GetTableDescriptorByTag
title: IISDB_CDT::GetTableDescriptorByTag (dvbsiparser.h)
description: Searches a subtable in an Integrated Services Digital Broadcasting (ISDB) common data table (CDT).
helpviewer_keywords: ["GetTableDescriptorByTag","GetTableDescriptorByTag method [Microsoft TV Technologies]","GetTableDescriptorByTag method [Microsoft TV Technologies]","IISDB_CDT interface","IISDB_CDT interface [Microsoft TV Technologies]","GetTableDescriptorByTag method","IISDB_CDT.GetTableDescriptorByTag","IISDB_CDT::GetTableDescriptorByTag","dvbsiparser/IISDB_CDT::GetTableDescriptorByTag","mstv.iisdb_cdt_gettabledescriptorbytag"]
old-location: mstv\iisdb_cdt_gettabledescriptorbytag.htm
tech.root: mstv
ms.assetid: c06f9d03-a46a-4c3f-bacc-a78f79c411c3
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByTag, GetTableDescriptorByTag method [Microsoft TV Technologies], GetTableDescriptorByTag method [Microsoft TV Technologies],IISDB_CDT interface, IISDB_CDT interface [Microsoft TV Technologies],GetTableDescriptorByTag method, IISDB_CDT.GetTableDescriptorByTag, IISDB_CDT::GetTableDescriptorByTag, dvbsiparser/IISDB_CDT::GetTableDescriptorByTag, mstv.iisdb_cdt_gettabledescriptorbytag
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
 - IISDB_CDT::GetTableDescriptorByTag
 - dvbsiparser/IISDB_CDT::GetTableDescriptorByTag
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
 - IISDB_CDT.GetTableDescriptorByTag
---

# IISDB_CDT::GetTableDescriptorByTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Searches a subtable in
  an Integrated Services Digital Broadcasting (ISDB)
  common data table (CDT).

## -parameters

### -param bTag [in]

Specifies the descriptor tag for which to search.

### -param pdwCookie [in, out]

Pointer to a variable that specifies the start position
  in the descriptor list. This parameter is optional.
  If the value of <i>pdwCookie</i> is <b>NULL</b>, the search starts from the
  first descriptor in the list. Otherwise, the search starts from
  the position given in <i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i> parameter contains the position of the next matching descriptor,
  if any. You can use this parameter to iterate through the descriptor list,
  looking for every instance of a particular descriptor tag.

### -param ppDescriptor [out]

Receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information
  in the descriptor. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdb_cdt">IISDB_CDT</a>
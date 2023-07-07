---
UID: NF:dvbsiparser.IPBDA_EIT.GetRecordDescriptorByIndex
title: IPBDA_EIT::GetRecordDescriptorByIndex (dvbsiparser.h)
description: Retrieves a descriptor for a specified record in an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetRecordDescriptorByIndex","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","GetRecordDescriptorByIndex method [Microsoft TV Technologies]","IPBDA_EIT interface","IPBDA_EIT interface [Microsoft TV Technologies]","GetRecordDescriptorByIndex method","IPBDA_EIT.GetRecordDescriptorByIndex","IPBDA_EIT::GetRecordDescriptorByIndex","dvbsiparser/IPBDA_EIT::GetRecordDescriptorByIndex","mstv.ipbda_eit_getrecorddescriptorbyindex"]
old-location: mstv\ipbda_eit_getrecorddescriptorbyindex.htm
tech.root: mstv
ms.assetid: 96ca5a6b-c515-4854-8e95-9cb155879b3b
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByIndex, GetRecordDescriptorByIndex method [Microsoft TV Technologies], GetRecordDescriptorByIndex method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetRecordDescriptorByIndex method, IPBDA_EIT.GetRecordDescriptorByIndex, IPBDA_EIT::GetRecordDescriptorByIndex, dvbsiparser/IPBDA_EIT::GetRecordDescriptorByIndex, mstv.ipbda_eit_getrecorddescriptorbyindex
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPBDA_EIT::GetRecordDescriptorByIndex
 - dvbsiparser/IPBDA_EIT::GetRecordDescriptorByIndex
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
 - IPBDA_EIT.GetRecordDescriptorByIndex
---

# IPBDA_EIT::GetRecordDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Retrieves a descriptor for a specified record in an  event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getcountofrecords">IPBDA_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.

### -param dwIndex [in]

Specifies the descriptor to retrieve, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getrecordcountofdescriptors">IPBDA_EIT::GetRecordCountOfDescriptors</a> method to get the number of descriptors for a particular record.

### -param ppDescriptor [out]

Address of a variable that receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>
---
UID: NF:dvbsiparser.IPBDA_EIT.GetRecordDescriptorByTag
title: IPBDA_EIT::GetRecordDescriptorByTag (dvbsiparser.h)
description: Searches a record in an event information table (EIT) from a Protected Broadcast Device Architecture (PBDA) transport stream for a descriptor with a specified descriptor tag.helpviewer_keywords: ["GetRecordDescriptorByTag","GetRecordDescriptorByTag method [Microsoft TV Technologies]","GetRecordDescriptorByTag method [Microsoft TV Technologies]","IPBDA_EIT interface","IPBDA_EIT interface [Microsoft TV Technologies]","GetRecordDescriptorByTag method","IPBDA_EIT.GetRecordDescriptorByTag","IPBDA_EIT::GetRecordDescriptorByTag","dvbsiparser/IPBDA_EIT::GetRecordDescriptorByTag","mstv.ipbda_eit_getrecorddescriptorbytag"]
old-location: mstv\ipbda_eit_getrecorddescriptorbytag.htm
tech.root: mstv
ms.assetid: d3c711e1-956f-4339-bcaf-78818da540f6
ms.date: 12/05/2018
ms.keywords: GetRecordDescriptorByTag, GetRecordDescriptorByTag method [Microsoft TV Technologies], GetRecordDescriptorByTag method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetRecordDescriptorByTag method, IPBDA_EIT.GetRecordDescriptorByTag, IPBDA_EIT::GetRecordDescriptorByTag, dvbsiparser/IPBDA_EIT::GetRecordDescriptorByTag, mstv.ipbda_eit_getrecorddescriptorbytag
f1_keywords:
- dvbsiparser/IPBDA_EIT.GetRecordDescriptorByTag
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IPBDA_EIT.GetRecordDescriptorByTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPBDA_EIT::GetRecordDescriptorByTag


## -description


Searches a record in an event information table (EIT) from a Protected Broadcast  Device Architecture (PBDA) transport stream for a descriptor with a specified descriptor tag. 


## -parameters




### -param dwRecordIndex [in]

Specifies the service record number, indexed from zero.
  Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-ipbda_eit-getcountofrecords">IPBDA_EIT::GetCountOfRecords</a> method to get the number of records in the EIT.



### -param bTag [in]

Specifies the descriptor tag for which to search.


### -param pdwCookie [in, out]

Pointer to a variable that specifies the start position in the descriptor list. This parameter is optional. If the value of *<i>pdwCookie</i> is <b>NULL</b>, the search starts from the first descriptor in the list. Otherwise, the search starts from the position given in *<i>pdwCookie</i>. When the method returns, the *<i>pdwCookie</i> parameter contains the position of the next matching descriptor, if any. You can use this parameter to iterate through the descriptor list, looking for every instance of a particular descriptor tag.


### -param ppDescriptor [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface. Use this interface to retrieve the information in the descriptor. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>
 

 


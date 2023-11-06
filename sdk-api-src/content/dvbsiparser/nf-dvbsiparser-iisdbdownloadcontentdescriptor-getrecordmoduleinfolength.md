---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleInfoLength
title: IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength (dvbsiparser.h)
description: Gets the value of the module_info_length field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The module_info_length field gives the length of the module_info_byte field in the descriptor.
helpviewer_keywords: ["GetRecordModuleInfoLength","GetRecordModuleInfoLength method [Microsoft TV Technologies]","GetRecordModuleInfoLength method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetRecordModuleInfoLength method","IIsdbDownloadContentDescriptor.GetRecordModuleInfoLength","IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength","dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength","mstv.iisdbdownloadcontentdescriptor_getrecordmoduleinfolength"]
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmoduleinfolength.htm
tech.root: mstv
ms.assetid: 963f44be-e0f4-4cb7-8e71-8641af0cd700
ms.date: 12/05/2018
ms.keywords: GetRecordModuleInfoLength, GetRecordModuleInfoLength method [Microsoft TV Technologies], GetRecordModuleInfoLength method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleInfoLength method, IIsdbDownloadContentDescriptor.GetRecordModuleInfoLength, IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength, mstv.iisdbdownloadcontentdescriptor_getrecordmoduleinfolength
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
 - IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength
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
 - IIsdbDownloadContentDescriptor.GetRecordModuleInfoLength
---

# IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the  value of the module_info_length field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The module_info_length field gives the length of the module_info_byte field in the descriptor.

## -parameters

### -param wRecordIndex [in]

Specifies the record number for the module containing the module_info_byte field,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a> method    to get the number of records in the extended event descriptor.

### -param pbVal [out]

Receives the length of the module_info_byte field. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getrecordmoduleinfo">IIsdbDownloadContentDescriptor::GetRecordModuleInfo</a> method to get the contents of this field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getrecordmoduleinfo">IIsdbDownloadContentDescriptor::GetRecordModuleInfo</a>
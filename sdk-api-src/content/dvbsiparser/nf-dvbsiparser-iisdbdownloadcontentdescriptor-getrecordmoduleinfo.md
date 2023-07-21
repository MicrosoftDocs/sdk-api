---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleInfo
title: IIsdbDownloadContentDescriptor::GetRecordModuleInfo (dvbsiparser.h)
description: Gets the value of a module_info_byte field from a module record in an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
helpviewer_keywords: ["GetRecordModuleInfo","GetRecordModuleInfo method [Microsoft TV Technologies]","GetRecordModuleInfo method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetRecordModuleInfo method","IIsdbDownloadContentDescriptor.GetRecordModuleInfo","IIsdbDownloadContentDescriptor::GetRecordModuleInfo","dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfo","mstv.iisdbdownloadcontentdescriptor_getrecordmoduleinfo"]
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmoduleinfo.htm
tech.root: mstv
ms.assetid: 0f9dc48c-7df3-498b-b9ff-4610bd9e7ac2
ms.date: 12/05/2018
ms.keywords: GetRecordModuleInfo, GetRecordModuleInfo method [Microsoft TV Technologies], GetRecordModuleInfo method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleInfo method, IIsdbDownloadContentDescriptor.GetRecordModuleInfo, IIsdbDownloadContentDescriptor::GetRecordModuleInfo, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfo, mstv.iisdbdownloadcontentdescriptor_getrecordmoduleinfo
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
 - IIsdbDownloadContentDescriptor::GetRecordModuleInfo
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfo
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
 - IIsdbDownloadContentDescriptor.GetRecordModuleInfo
---

# IIsdbDownloadContentDescriptor::GetRecordModuleInfo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the value of a module_info_byte field from a module record in an Integrated Services Digital Broadcasting (ISDB) download content descriptor. This field can include the type, name, information, or control descriptor from the download information indication (DII) message.

## -parameters

### -param wRecordIndex [in]

Specifies the record number for the module containing the module_info_byte field,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param ppbData [out]

Pointer to a buffer that receives the field value. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>
---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleSize
title: IIsdbDownloadContentDescriptor::GetRecordModuleSize (dvbsiparser.h)
description: Gets the size of a module from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.
helpviewer_keywords: ["GetRecordModuleSize","GetRecordModuleSize method [Microsoft TV Technologies]","GetRecordModuleSize method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetRecordModuleSize method","IIsdbDownloadContentDescriptor.GetRecordModuleSize","IIsdbDownloadContentDescriptor::GetRecordModuleSize","dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleSize","mstv.iisdbdownloadcontentdescriptor_getrecordmodulesize"]
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmodulesize.htm
tech.root: mstv
ms.assetid: 395264ee-63de-4de4-bd28-4d5c4634dcf3
ms.date: 12/05/2018
ms.keywords: GetRecordModuleSize, GetRecordModuleSize method [Microsoft TV Technologies], GetRecordModuleSize method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleSize method, IIsdbDownloadContentDescriptor.GetRecordModuleSize, IIsdbDownloadContentDescriptor::GetRecordModuleSize, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleSize, mstv.iisdbdownloadcontentdescriptor_getrecordmodulesize
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
 - IIsdbDownloadContentDescriptor::GetRecordModuleSize
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleSize
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
 - IIsdbDownloadContentDescriptor.GetRecordModuleSize
---

# IIsdbDownloadContentDescriptor::GetRecordModuleSize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the size of a module from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.

## -parameters

### -param wRecordIndex [in]

Specifies the record number for the module containing the module_info_byte field,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a> method    to get the number of records in the download content descriptor.

### -param pdwVal [out]

Receives the module size.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>
---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleId
title: IIsdbDownloadContentDescriptor::GetRecordModuleId
author: windows-sdk-content
description: Gets the identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor that specifies the carousel used for downloading.
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmoduleid.htm
old-project: mstv
ms.assetid: c714b2f2-e787-40cc-b57b-d56b54dc8966
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordModuleId, GetRecordModuleId method [Microsoft TV Technologies], GetRecordModuleId method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleId method, IIsdbDownloadContentDescriptor.GetRecordModuleId, IIsdbDownloadContentDescriptor::GetRecordModuleId, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleId, mstv.iisdbdownloadcontentdescriptor_getrecordmoduleid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.redist: 
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
tech.root: 
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IIsdbDownloadContentDescriptor.GetRecordModuleId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDownloadContentDescriptor::GetRecordModuleId


## -description


 Gets the identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor that specifies the carousel used for downloading.


## -parameters




### -param wRecordIndex [in]

Specifies the module record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>method to get the number of records in the extended event descriptor.


### -param pwVal [out]

Receives the module ID.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>



<a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>
 

 


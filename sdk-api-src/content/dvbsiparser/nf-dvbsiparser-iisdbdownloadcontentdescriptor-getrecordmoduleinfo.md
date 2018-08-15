---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleInfo
title: IIsdbDownloadContentDescriptor::GetRecordModuleInfo
author: windows-sdk-content
description: Gets the value of a module_info_byte field from a module record in an Integrated Services Digital Broadcasting (ISDB) download content descriptor.
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmoduleinfo.htm
old-project: mstv
ms.assetid: 0f9dc48c-7df3-498b-b9ff-4610bd9e7ac2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordModuleInfo, GetRecordModuleInfo method [Microsoft TV Technologies], GetRecordModuleInfo method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleInfo method, IIsdbDownloadContentDescriptor.GetRecordModuleInfo, IIsdbDownloadContentDescriptor::GetRecordModuleInfo, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfo, mstv.iisdbdownloadcontentdescriptor_getrecordmoduleinfo
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
 - IIsdbDownloadContentDescriptor.GetRecordModuleInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDownloadContentDescriptor::GetRecordModuleInfo


## -description


 Gets the value of a module_info_byte field from a module record in an Integrated Services Digital Broadcasting (ISDB) download content descriptor. This field can include the type, name, information, or control descriptor from the download information indication (DII) message.


## -parameters




### -param wRecordIndex [in]

Specifies the record number for the module containing the module_info_byte field,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>method to get the number of records in the extended event descriptor.


### -param ppbData [out]

Pointer to a buffer that receives the field value. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>



<a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>
 

 


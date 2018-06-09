---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleInfoLength
title: IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength
author: windows-sdk-content
description: Gets the value of the module_info_length field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The module_info_length field gives the length of the module_info_byte field in the descriptor.
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmoduleinfolength.htm
old-project: mstv
ms.assetid: 963f44be-e0f4-4cb7-8e71-8641af0cd700
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: GetRecordModuleInfoLength, GetRecordModuleInfoLength method [Microsoft TV Technologies], GetRecordModuleInfoLength method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleInfoLength method, IIsdbDownloadContentDescriptor.GetRecordModuleInfoLength, IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength, mstv.iisdbdownloadcontentdescriptor_getrecordmoduleinfolength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IIsdbDownloadContentDescriptor.GetRecordModuleInfoLength
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbDownloadContentDescriptor::GetRecordModuleInfoLength


## -description


Gets the  value of the module_info_length field from an Integrated Services Digital Broadcasting (ISDB) download content descriptor. The module_info_length field gives the length of the module_info_byte field in the descriptor.


## -parameters




### -param wRecordIndex [in]

Specifies the record number for the module containing the module_info_byte field,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>
  method    to get the number of records in the extended event descriptor.


### -param pbVal [out]

Receives the length of the module_info_byte field. Call the <a href="https://msdn.microsoft.com/0f9dc48c-7df3-498b-b9ff-4610bd9e7ac2">IIsdbDownloadContentDescriptor::GetRecordModuleInfo</a> method to get the contents of this field.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>



<a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>



<a href="https://msdn.microsoft.com/0f9dc48c-7df3-498b-b9ff-4610bd9e7ac2">IIsdbDownloadContentDescriptor::GetRecordModuleInfo</a>
 

 


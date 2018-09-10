---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleSize
title: IIsdbDownloadContentDescriptor::GetRecordModuleSize
author: windows-sdk-content
description: Gets the size of a module from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmodulesize.htm
tech.root: mstv
ms.assetid: 395264ee-63de-4de4-bd28-4d5c4634dcf3
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetRecordModuleSize, GetRecordModuleSize method [Microsoft TV Technologies], GetRecordModuleSize method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleSize method, IIsdbDownloadContentDescriptor.GetRecordModuleSize, IIsdbDownloadContentDescriptor::GetRecordModuleSize, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleSize, mstv.iisdbdownloadcontentdescriptor_getrecordmodulesize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IIsdbDownloadContentDescriptor.GetRecordModuleSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDownloadContentDescriptor::GetRecordModuleSize


## -description


 Gets the size of a module from an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.


## -parameters




### -param wRecordIndex [in]

Specifies the record number for the module containing the module_info_byte field,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>method    to get the number of records in the download content descriptor.


### -param pdwVal [out]

Receives the module size.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/beef626c-64b1-4f49-bb21-69022907004d">IIsdbDownloadContentDescriptor</a>



<a href="https://msdn.microsoft.com/d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>
 

 


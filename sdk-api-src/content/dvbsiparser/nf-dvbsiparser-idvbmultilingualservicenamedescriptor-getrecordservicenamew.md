---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetRecordServiceNameW
title: IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW method
author: windows-driver-content
description: Gets the service name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor.
old-location: mstv\idvbmultilingualservicenamedescriptor_getrecordservicenamew.htm
old-project: mstv
ms.assetid: dfe9040d-18f1-4a35-a4ed-bb3f84ad8dd7
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetRecordServiceNameW method [Microsoft TV Technologies], GetRecordServiceNameW method [Microsoft TV Technologies], IDvbMultilingualServiceNameDescriptor interface, GetRecordServiceNameW,IDvbMultilingualServiceNameDescriptor.GetRecordServiceNameW, IDvbMultilingualServiceNameDescriptor, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies], GetRecordServiceNameW method, IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW, mstv.idvbmultilingualservicenamedescriptor_getrecordservicenamew
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDvbMultilingualServiceNameDescriptor.GetRecordServiceNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW method


## -description


Gets the service name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/c157e520-696f-45d8-8e43-0e6845882404">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a>
  method to get the number of records in the logical channel descriptor.


### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to a buffer that receives the service name string. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b384ecf-aa56-476d-b347-b5438ab069fe">IDvbMultilingualServiceNameDescriptor</a>



<a href="https://msdn.microsoft.com/c157e520-696f-45d8-8e43-0e6845882404">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a>
 

 


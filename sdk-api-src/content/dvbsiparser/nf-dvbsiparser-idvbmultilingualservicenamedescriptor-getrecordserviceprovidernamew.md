---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetRecordServiceProviderNameW
title: IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW method
author: windows-driver-content
description: Gets the service provider name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor.
old-location: mstv\idvbmultilingualservicenamedescriptor_getrecordserviceprovidernamew.htm
old-project: mstv
ms.assetid: e07ebe5c-b5b3-4604-91c3-3e75042ad074
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetRecordServiceProviderNameW method [Microsoft TV Technologies], GetRecordServiceProviderNameW method [Microsoft TV Technologies], IDvbMultilingualServiceNameDescriptor interface, GetRecordServiceProviderNameW,IDvbMultilingualServiceNameDescriptor.GetRecordServiceProviderNameW, IDvbMultilingualServiceNameDescriptor, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies], GetRecordServiceProviderNameW method, IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW, mstv.idvbmultilingualservicenamedescriptor_getrecordserviceprovidernamew
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
-	IDvbMultilingualServiceNameDescriptor.GetRecordServiceProviderNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW method


## -description


Gets the service provider name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor. 


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

Pointer to a memory block that receives the service provider name string. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1b384ecf-aa56-476d-b347-b5438ab069fe">IDvbMultilingualServiceNameDescriptor</a>



<a href="https://msdn.microsoft.com/c157e520-696f-45d8-8e43-0e6845882404">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a>
 

 


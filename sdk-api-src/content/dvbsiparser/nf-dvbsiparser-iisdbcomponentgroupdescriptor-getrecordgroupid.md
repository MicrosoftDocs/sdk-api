---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordGroupId
title: IIsdbComponentGroupDescriptor::GetRecordGroupId (dvbsiparser.h)
author: windows-sdk-content
description: Gets the component group identifier from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordgroupid.htm
tech.root: mstv
ms.assetid: 159c496c-675e-458a-b9f9-5c9622fd1848
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetRecordGroupId, GetRecordGroupId method [Microsoft TV Technologies], GetRecordGroupId method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordGroupId method, IIsdbComponentGroupDescriptor.GetRecordGroupId, IIsdbComponentGroupDescriptor::GetRecordGroupId, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordGroupId, mstv.iisdbcomponentgroupdescriptor_getrecordgroupid
ms.topic: method
f1_keywords: 
 - "dvbsiparser/IIsdbComponentGroupDescriptor.GetRecordGroupId"
dev_langs:
 - c++
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
 - IIsdbComponentGroupDescriptor.GetRecordGroupId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbComponentGroupDescriptor::GetRecordGroupId


## -description


Gets the component group identifier from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>method to get the number of records in the extended event descriptor.


### -param pbVal [out]

Receives the component group record number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>
 

 


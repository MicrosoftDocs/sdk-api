---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordTotalBitRate
title: IIsdbComponentGroupDescriptor::GetRecordTotalBitRate (dvbsiparser.h)
description: Gets the total bit rate from a component within a component group in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.helpviewer_keywords: ["GetRecordTotalBitRate","GetRecordTotalBitRate method [Microsoft TV Technologies]","GetRecordTotalBitRate method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetRecordTotalBitRate method","IIsdbComponentGroupDescriptor.GetRecordTotalBitRate","IIsdbComponentGroupDescriptor::GetRecordTotalBitRate","dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordTotalBitRate","mstv.iisdbcomponentgroupdescriptor_getrecordtotalbitrate"]
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordtotalbitrate.htm
tech.root: mstv
ms.assetid: 7c84dc9f-933c-4fc8-982c-1f311b94ddf4
ms.date: 12/05/2018
ms.keywords: GetRecordTotalBitRate, GetRecordTotalBitRate method [Microsoft TV Technologies], GetRecordTotalBitRate method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordTotalBitRate method, IIsdbComponentGroupDescriptor.GetRecordTotalBitRate, IIsdbComponentGroupDescriptor::GetRecordTotalBitRate, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordTotalBitRate, mstv.iisdbcomponentgroupdescriptor_getrecordtotalbitrate
f1_keywords:
- dvbsiparser/IIsdbComponentGroupDescriptor.GetRecordTotalBitRate
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
- IIsdbComponentGroupDescriptor.GetRecordTotalBitRate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbComponentGroupDescriptor::GetRecordTotalBitRate


## -description


 Gets the total bit rate from a component within a component group in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>method to get the number of records in the extended event descriptor.


### -param pbVal [out]

Receives the total bit rate for the component, in units of 250 Kbps.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>
 

 


---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordTextW
title: IIsdbComponentGroupDescriptor::GetRecordTextW (dvbsiparser.h)
description: Gets the text that describes a component group from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetRecordTextW","GetRecordTextW method [Microsoft TV Technologies]","GetRecordTextW method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetRecordTextW method","IIsdbComponentGroupDescriptor.GetRecordTextW","IIsdbComponentGroupDescriptor::GetRecordTextW","dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordTextW","mstv.iisdbcomponentgroupdescriptor_getrecordtextw"]
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordtextw.htm
tech.root: mstv
ms.assetid: 0aea8704-cda0-44d5-b06d-79db6ce0114e
ms.date: 12/05/2018
ms.keywords: GetRecordTextW, GetRecordTextW method [Microsoft TV Technologies], GetRecordTextW method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordTextW method, IIsdbComponentGroupDescriptor.GetRecordTextW, IIsdbComponentGroupDescriptor::GetRecordTextW, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordTextW, mstv.iisdbcomponentgroupdescriptor_getrecordtextw
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
 - IIsdbComponentGroupDescriptor::GetRecordTextW
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordTextW
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
 - IIsdbComponentGroupDescriptor.GetRecordTextW
---

# IIsdbComponentGroupDescriptor::GetRecordTextW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the text that describes a component group from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrText [out]

Receives the text that describes the component group, as a <b>BSTR</b>. The caller must free the <b>BSTR</b> by calling <b>SysFreeString</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>
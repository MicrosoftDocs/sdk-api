---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetTSNameW
title: IIsdbTSInformationDescriptor::GetTSNameW (dvbsiparser.h)
description: Gets the transport stream name from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor, in Unicode string format.
helpviewer_keywords: ["GetTSNameW","GetTSNameW method [Microsoft TV Technologies]","GetTSNameW method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetTSNameW method","IIsdbTSInformationDescriptor.GetTSNameW","IIsdbTSInformationDescriptor::GetTSNameW","dvbsiparser/IIsdbTSInformationDescriptor::GetTSNameW","mstv.iisdbtsinformationdescriptor_gettsnamew"]
old-location: mstv\iisdbtsinformationdescriptor_gettsnamew.htm
tech.root: mstv
ms.assetid: 4c8900d1-1047-4b11-87e0-da1a72f511f7
ms.date: 12/05/2018
ms.keywords: GetTSNameW, GetTSNameW method [Microsoft TV Technologies], GetTSNameW method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetTSNameW method, IIsdbTSInformationDescriptor.GetTSNameW, IIsdbTSInformationDescriptor::GetTSNameW, dvbsiparser/IIsdbTSInformationDescriptor::GetTSNameW, mstv.iisdbtsinformationdescriptor_gettsnamew
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbTSInformationDescriptor::GetTSNameW
 - dvbsiparser/IIsdbTSInformationDescriptor::GetTSNameW
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
 - IIsdbTSInformationDescriptor.GetTSNameW
---

# IIsdbTSInformationDescriptor::GetTSNameW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the transport stream name  from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor, in Unicode string format.

## -parameters

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrName [out]

Pointer to a buffer that receives the transport stream name. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>
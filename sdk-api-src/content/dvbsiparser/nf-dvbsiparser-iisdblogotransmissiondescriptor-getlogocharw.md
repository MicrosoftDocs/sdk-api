---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetLogoCharW
title: IIsdbLogoTransmissionDescriptor::GetLogoCharW (dvbsiparser.h)
description: Gets the character string for a simple logo from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
helpviewer_keywords: ["GetLogoCharW","GetLogoCharW method [Microsoft TV Technologies]","GetLogoCharW method [Microsoft TV Technologies]","IIsdbLogoTransmissionDescriptor interface","IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies]","GetLogoCharW method","IIsdbLogoTransmissionDescriptor.GetLogoCharW","IIsdbLogoTransmissionDescriptor::GetLogoCharW","dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoCharW","mstv.iisdblogotransmissiondescriptor_getlogocharw"]
old-location: mstv\iisdblogotransmissiondescriptor_getlogocharw.htm
tech.root: mstv
ms.assetid: bb4ba9f1-f633-4cb4-adc4-6671bb5fc239
ms.date: 12/05/2018
ms.keywords: GetLogoCharW, GetLogoCharW method [Microsoft TV Technologies], GetLogoCharW method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetLogoCharW method, IIsdbLogoTransmissionDescriptor.GetLogoCharW, IIsdbLogoTransmissionDescriptor::GetLogoCharW, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoCharW, mstv.iisdblogotransmissiondescriptor_getlogocharw
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
 - IIsdbLogoTransmissionDescriptor::GetLogoCharW
 - dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoCharW
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
 - IIsdbLogoTransmissionDescriptor.GetLogoCharW
---

# IIsdbLogoTransmissionDescriptor::GetLogoCharW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the character string for a simple logo from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.

## -parameters

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrChar [out]

Pointer to a buffer that receives the logo text. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdblogotransmissiondescriptor">IIsdbLogoTransmissionDescriptor</a>
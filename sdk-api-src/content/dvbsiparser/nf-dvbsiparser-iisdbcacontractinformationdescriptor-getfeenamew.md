---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetFeeNameW
title: IIsdbCAContractInformationDescriptor::GetFeeNameW (dvbsiparser.h)
description: Gets, in Unicode-text format, the value of the fee_name field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field describes the fee for the ES group being described.
helpviewer_keywords: ["GetFeeNameW","GetFeeNameW method [Microsoft TV Technologies]","GetFeeNameW method [Microsoft TV Technologies]","IIsdbCAContractInformationDescriptor interface","IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies]","GetFeeNameW method","IIsdbCAContractInformationDescriptor.GetFeeNameW","IIsdbCAContractInformationDescriptor::GetFeeNameW","dvbsiparser/IIsdbCAContractInformationDescriptor::GetFeeNameW","mstv.iisdbcacontractinformationdescriptor_getfeenamew"]
old-location: mstv\iisdbcacontractinformationdescriptor_getfeenamew.htm
tech.root: mstv
ms.assetid: c2fcdcc1-acca-417e-bcf5-baad4ea07cef
ms.date: 12/05/2018
ms.keywords: GetFeeNameW, GetFeeNameW method [Microsoft TV Technologies], GetFeeNameW method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetFeeNameW method, IIsdbCAContractInformationDescriptor.GetFeeNameW, IIsdbCAContractInformationDescriptor::GetFeeNameW, dvbsiparser/IIsdbCAContractInformationDescriptor::GetFeeNameW, mstv.iisdbcacontractinformationdescriptor_getfeenamew
f1_keywords:
- dvbsiparser/IIsdbCAContractInformationDescriptor.GetFeeNameW
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbCAContractInformationDescriptor.GetFeeNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbCAContractInformationDescriptor::GetFeeNameW


## -description


Gets, in Unicode-text format, the value of the fee_name field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field describes the fee for the ES group being described.


## -parameters




### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>



### -param pbstrName [out]

Pointer to a buffer that receives the fee name. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcacontractinformationdescriptor">IIsdbCAContractInformationDescriptor</a>
 

 


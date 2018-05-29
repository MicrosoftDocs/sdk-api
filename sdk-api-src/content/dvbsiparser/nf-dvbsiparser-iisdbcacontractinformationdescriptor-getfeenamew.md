---
UID: NF:dvbsiparser.IIsdbCAContractInformationDescriptor.GetFeeNameW
title: IIsdbCAContractInformationDescriptor::GetFeeNameW
author: windows-sdk-content
description: Gets, in Unicode-text format, the value of the fee_name field from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) contract information descriptor. This field describes the fee for the ES group being described.
old-location: mstv\iisdbcacontractinformationdescriptor_getfeenamew.htm
old-project: mstv
ms.assetid: c2fcdcc1-acca-417e-bcf5-baad4ea07cef
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetFeeNameW, GetFeeNameW method [Microsoft TV Technologies], GetFeeNameW method [Microsoft TV Technologies],IIsdbCAContractInformationDescriptor interface, IIsdbCAContractInformationDescriptor interface [Microsoft TV Technologies],GetFeeNameW method, IIsdbCAContractInformationDescriptor.GetFeeNameW, IIsdbCAContractInformationDescriptor::GetFeeNameW, dvbsiparser/IIsdbCAContractInformationDescriptor::GetFeeNameW, mstv.iisdbcacontractinformationdescriptor_getfeenamew
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbCAContractInformationDescriptor.GetFeeNameW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
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




<a href="https://msdn.microsoft.com/d877a625-d683-4472-98de-f24c165c753a">IIsdbCAContractInformationDescriptor</a>
 

 


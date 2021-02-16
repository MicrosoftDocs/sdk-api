---
UID: NF:mswmdm.ISCPSecureQuery.ExamineData
title: ISCPSecureQuery::ExamineData (mswmdm.h)
description: The ExamineData method determines rights and responsibility for the content by examining data that Windows Media Device Manager passes to this method.
helpviewer_keywords: ["ExamineData","ExamineData method [windows Media Device Manager]","ExamineData method [windows Media Device Manager]","ISCPSecureQuery interface","ISCPSecureQuery interface [windows Media Device Manager]","ExamineData method","ISCPSecureQuery.ExamineData","ISCPSecureQuery::ExamineData","ISCPSecureQueryExamineData","mswmdm/ISCPSecureQuery::ExamineData","wmdm.iscpsecurequery_examinedata"]
old-location: wmdm\iscpsecurequery_examinedata.htm
tech.root: WMDM
ms.assetid: e12d8b55-5600-4178-8b2b-8afe8ade6818
ms.date: 12/05/2018
ms.keywords: ExamineData, ExamineData method [windows Media Device Manager], ExamineData method [windows Media Device Manager],ISCPSecureQuery interface, ISCPSecureQuery interface [windows Media Device Manager],ExamineData method, ISCPSecureQuery.ExamineData, ISCPSecureQuery::ExamineData, ISCPSecureQueryExamineData, mswmdm/ISCPSecureQuery::ExamineData, wmdm.iscpsecurequery_examinedata
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISCPSecureQuery::ExamineData
 - mswmdm/ISCPSecureQuery::ExamineData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - ISCPSecureQuery.ExamineData
---

# ISCPSecureQuery::ExamineData


## -description

The <b>ExamineData</b> method determines rights and responsibility for the content by examining data that Windows Media Device Manager passes to this method.

## -parameters

### -param fuFlags [in]

Flags describing the data offered to the secure content provider to make decisions. The following flags can be present.

<table>
<tr>
<th>Flag
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>WMDM_SCP_EXAMINE_DATA</td>
<td>The <i>pData</i> parameter points to data to be examined.</td>
</tr>
</table>

### -param pwszExtension [in]

Pointer to the file name extension to be examined if the secure content provider asks for an extension in the <a href="/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery-getdatademands">GetDataDemands</a> call.

### -param pData [in]

Pointer to the data at the beginning of the file to be examined. This parameter must be included in the input message authentication code and must be encrypted.

### -param dwSize [in]

<b>DWORD</b> that contains the length, in bytes, of the data to be examined. This parameter must be included in the input message authentication code.

### -param abMac [in, out]

Array of eight bytes containing the message authentication code for the parameter data of this method. (WMDM_MAC_LENGTH is defined as 8.)

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded. The secure content provider is responsible for this content.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_CALL_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
This method was called out of sequence. <b>GetDataDemands</b> must be called first.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_MAC_CHECK_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The message authentication code is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WMDM_E_MOREDATA</b></dt>
</dl>
</td>
<td width="60%">
Windows Media Device Manager must call this method again with another packet of data. The size of the packet is determined by the <i>pdwMinExamineData</i> parameter in the <b>GetDataDemands</b> method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The secure content provider is not responsible for this content. Terminate interaction with the secure content provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid or is a <b>NULL</b> pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -remarks

This method is called after the <b>GetDataDemands</b> method. The secure content provider uses the information passed in this method to determine whether it is responsible for the content. The <i>fuFlags</i> parameter is consulted to determine which data has been presented for examination. The <i>pData</i> parameter points to the beginning of the rights and responsibility data. The <i>dwSize</i> parameter contains the length, in bytes, of the rights and responsibility data.

If the WMDM_SCP_EXAMINE_DATA flag is set, then the <i>pDataBuffer</i> parameter contains <i>dwDataLength</i> of bytes for the secure content provider to examine.

If this method does not return S_OK or WMDM_E_MOREDATA, then Windows Media Device Manager does not make any further calls to this secure content provider.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>
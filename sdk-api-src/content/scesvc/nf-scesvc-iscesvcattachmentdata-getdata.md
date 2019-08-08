---
UID: NF:scesvc.ISceSvcAttachmentData.GetData
title: ISceSvcAttachmentData::GetData (scesvc.h)
author: windows-sdk-content
description: The GetData method retrieves configuration information from the Security Configuration snap-in.
old-location: security\iscesvcattachmentdata_getdata.htm
tech.root: SecMgmt
ms.assetid: f0b51592-58d9-45f2-a0a5-7cdbde0bc0a1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetData, GetData method [Security], GetData method [Security],ISceSvcAttachmentData interface, ISceSvcAttachmentData interface [Security],GetData method, ISceSvcAttachmentData.GetData, ISceSvcAttachmentData::GetData, SCE_SERVICE_ANALYSIS_INFO, SCE_SERVICE_CONFIGURATION_INFO, _config_iscesvcattachmentdata_getdata, scesvc/ISceSvcAttachmentData::GetData, security.iscesvcattachmentdata_getdata
ms.topic: method
f1_keywords:
- scesvc/ISceSvcAttachmentData.GetData
req.header: scesvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Wsecedit.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wsecedit.dll
api_name:
- ISceSvcAttachmentData.GetData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISceSvcAttachmentData::GetData


## -description


The <b>GetData</b> method retrieves configuration information from the Security Configuration snap-in.


## -parameters




### -param scesvcHandle [in]

Type: <b>SCESVC_HANDLE</b>

A 
<a href="https://docs.microsoft.com/windows/desktop/SecMgmt/scesvc-handle">SCESVC_HANDLE</a> returned during a previous call to 
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-initialize">ISceSvcAttachmentData::Initialize</a>.


### -param sceType [in]

Type: <b>SCESVC_INFO_TYPE</b>

A 
<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/ne-scesvc-scesvc_info_type">SCESVC_INFO_TYPE</a> value that indicates the type of information requested from the security database. It can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCE_SERVICE_CONFIGURATION_INFO"></a><a id="sce_service_configuration_info"></a><dl>
<dt><b>SCE_SERVICE_CONFIGURATION_INFO</b></dt>
</dl>
</td>
<td width="60%">
Requests configuration information from the database.

</td>
</tr>
<tr>
<td width="40%"><a id="SCE_SERVICE_ANALYSIS_INFO"></a><a id="sce_service_analysis_info"></a><dl>
<dt><b>SCE_SERVICE_ANALYSIS_INFO</b></dt>
</dl>
</td>
<td width="60%">
Requests analysis information from the database.

</td>
</tr>
</table>
 


### -param ppvData [out]

Type: <b>PVOID*</b>

Pointer to a buffer which receives the data.


### -param psceEnumHandle [in, out]

Type: <b>PSCE_ENUMERATION_CONTEXT</b>

An opaque handle used to navigate through the security database.


## -returns



Type: <b>HRESULT</b>

The return value is an <b>HRESULT</b>. A value of S_OK indicates the method was successful.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nn-scesvc-iscesvcattachmentdata">ISceSvcAttachmentData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-initialize">ISceSvcAttachmentData::Initialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/scesvc/ne-scesvc-scesvc_info_type">SCESVC_INFO_TYPE</a>
 

 


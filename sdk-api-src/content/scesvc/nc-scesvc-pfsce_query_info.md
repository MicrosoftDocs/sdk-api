---
UID: NC:scesvc.PFSCE_QUERY_INFO
title: PFSCE_QUERY_INFO (scesvc.h)
author: windows-sdk-content
description: Queries service-specific information from the Security Configuration file or analysis database.
old-location: security\pfsce_query_info.htm
tech.root: SecMgmt
ms.assetid: a0e4a205-46d4-47c9-97cf-66f6bec34a1b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FALSE, PFSCE_QUERY_INFO, PFSCE_QUERY_INFO callback, PFSCE_QUERY_INFO callback function [Security], SCESVC_ANALYSIS_INFO, SCESVC_CONFIGURATION_INFO, SCE_SERVICE_ANALYSIS_INFO, SCE_SERVICE_CONFIGURATION_INFO, TRUE, _config_pfsce_query_info, scesvc/PFSCE_QUERY_INFO, security.pfsce_query_info
ms.topic: callback
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Scesvc.h
api_name:
 - PFSCE_QUERY_INFO
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFSCE_QUERY_INFO callback function


## -description


The <i>PFSCE_QUERY_INFO</i> callback function queries service-specific information from the Security Configuration file or analysis database.


## -parameters




### -param sceHandle [in]

Type: <b>SCE_HANDLE</b>

Specifies the opaque handle passed to the attachment by the Security Configuration tool set during the call to 
<a href="https://msdn.microsoft.com/2c5d087d-774b-4cfb-a458-9a5b1c6106c7">ISceSvcAttachmentData::Initialize</a>. This handle is used to store the queried information.


### -param sceType [in]

Type: <b>SCESVC_INFO_TYPE</b>

Specifies the type of information to be queried. Specify one of the following flags.

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
 


### -param lpPrefix [in, optional]

Type: <b>LPTSTR</b>

Specifies a prefix or key (see <i>bExact</i>) for limiting the query. When a string is supplied, only those keys (and their corresponding values) that match the string are returned. When set to <b>NULL</b>, all keys are returned.


### -param bExact [in]

Type: <b>BOOL</b>

Specifies whether the string provided by <i>lpPrefix</i> should be treated as a specific key or a prefix. This parameter is ignored if <i>lpPrefix</i> is set to <b>NULL</b>. Specify one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The string specified in <i>lpPrefix</i> represents a specific key. Only records matching that key are returned.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The string specified by <i>lpPrefix</i> represents a prefix. All keys (and their values) that have this same prefix are returned.

</td>
</tr>
</table>
 


### -param *ppvInfo [out]

Type: <b>PVOID*</b>

Returns a pointer to one of the following structures. The Security Configuration tool set (not the attachment) allocates the buffer for the information; therefore, this pointer must point to <b>NULL</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCESVC_CONFIGURATION_INFO"></a><a id="scesvc_configuration_info"></a><dl>
<dt><b>SCESVC_CONFIGURATION_INFO</b></dt>
</dl>
</td>
<td width="60%">
When <i>sceType</i> is set to SCE_SERVICE_CONFIGURATION_INFO.

</td>
</tr>
<tr>
<td width="40%"><a id="SCESVC_ANALYSIS_INFO"></a><a id="scesvc_analysis_info"></a><dl>
<dt><b>SCESVC_ANALYSIS_INFO</b></dt>
</dl>
</td>
<td width="60%">
When <i>sceType</i> is set to SCE_SERVICE_ANALYSIS_INFO.

</td>
</tr>
</table>
 


### -param psceEnumHandle [out]

Type: <b>PSCE_ENUMERATION_CONTEXT</b>

Returns a handle that can be used in successive calls to this function. Due to the large number of keys that may be present, not all keys are returned in a single call. The maximum number of keys that may be returned in a single call is 256.


## -returns



Type: <b>SCESTATUS</b>

An <b>SCESTATUS</b> value that indicates the result of the function call. If the function succeeds, it returns SCESTATUS_SUCCESS; otherwise, it returns an error value, which can be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters passed into the function was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified record was not found in the security database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The format is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_OTHER_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_NOT_ENOUGH_RESOURCE</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory.

</td>
</tr>
</table>
 




## -remarks



The Security Configuration tool set allocates buffers when <i>PFSCE_QUERY_INFO</i> is called. To free these buffers call 
<a href="https://msdn.microsoft.com/e7cafdbc-9ca2-4bb1-b8ed-d5553acaf7bc">PFSCE_FREE_INFO</a> after the returned information is no longer needed.


#### Examples

<table>
<tr>
<th>For an example of</th>
<th>See</th>
</tr>
<tr>
<td>Retrieving configuration information</td>
<td>
<a href="https://msdn.microsoft.com/c0c1c1e4-de5b-405d-abe8-33a985ce98e5">Implementing SceSvcAttachmentConfig</a>
</td>
</tr>
<tr>
<td>Retrieving analysis information</td>
<td>
<a href="https://msdn.microsoft.com/f8420dde-55a2-40a0-b10d-140c28c0e9e4">Implementing SceSvcAttachmentAnalyze</a>
</td>
</tr>
<tr>
<td>Retrieving configuration and analysis information</td>
<td>
<a href="https://msdn.microsoft.com/3c0a71f6-f643-4a5e-8b5c-15c976a3736e">Implementing SceSvcAttachmentUpdate</a>
</td>
</tr>
</table>
 

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e7cafdbc-9ca2-4bb1-b8ed-d5553acaf7bc">PFSCE_FREE_INFO</a>



<a href="https://msdn.microsoft.com/4f0273df-435d-4324-b8ce-a774da935059">SCESVC_ANALYSIS_INFO</a>



<a href="https://msdn.microsoft.com/a89ab072-7b7c-4ecd-83fa-26e2689778df">SCESVC_CONFIGURATION_INFO</a>
 

 


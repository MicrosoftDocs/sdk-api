---
UID: NC:scesvc.PFSCE_SET_INFO
title: PFSCE_SET_INFO (scesvc.h)
description: Sets or overwrites service-specific configuration and analysis information.
helpviewer_keywords: ["FALSE","PFSCE_SET_INFO","PFSCE_SET_INFO callback","PFSCE_SET_INFO callback function [Security]","SCESVC_ANALYSIS_INFO","SCESVC_CONFIGURATION_INFO","SCE_SERVICE_ANALYSIS_INFO","SCE_SERVICE_CONFIGURATION_INFO","TRUE","_config_pfsce_set_info","scesvc/PFSCE_SET_INFO","security.pfsce_set_info"]
old-location: security\pfsce_set_info.htm
tech.root: security
ms.assetid: 131585a9-b0a9-4686-84ba-237bcdcc4f5f
ms.date: 12/05/2018
ms.keywords: FALSE, PFSCE_SET_INFO, PFSCE_SET_INFO callback, PFSCE_SET_INFO callback function [Security], SCESVC_ANALYSIS_INFO, SCESVC_CONFIGURATION_INFO, SCE_SERVICE_ANALYSIS_INFO, SCE_SERVICE_CONFIGURATION_INFO, TRUE, _config_pfsce_set_info, scesvc/PFSCE_SET_INFO, security.pfsce_set_info
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFSCE_SET_INFO
 - scesvc/PFSCE_SET_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Scesvc.h
api_name:
 - PFSCE_SET_INFO
---

# PFSCE_SET_INFO callback function


## -description

The <i>PFSCE_SET_INFO</i> callback function sets or overwrites service-specific configuration and analysis information.

## -parameters

### -param sceHandle [in]

Type: <b>SCE_HANDLE</b>

Specifies the opaque SCE handle passed to the attachment by the Security Configuration tool set during the call to 
<a href="/windows/desktop/api/scesvc/nf-scesvc-iscesvcattachmentdata-initialize">ISceSvcAttachmentData::Initialize</a>. This handle is used to set or overwrite the information.

### -param sceType [in]

Type: <b>SCESVC_INFO_TYPE</b>

Specifies the type of information to be set. Specify one of the following flags.

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
Indicates that configuration information is set.

</td>
</tr>
<tr>
<td width="40%"><a id="SCE_SERVICE_ANALYSIS_INFO"></a><a id="sce_service_analysis_info"></a><dl>
<dt><b>SCE_SERVICE_ANALYSIS_INFO</b></dt>
</dl>
</td>
<td width="60%">
Indicates that analysis information is set.

</td>
</tr>
</table>

### -param lpPrefix [in, optional]

Type: <b>LPTSTR</b>

Specifies what information should be set or overwritten. This string can specify a specific key (see <i>bExact</i>) or a prefix for a set of keys. When a string is supplied, only information for those keys (and their corresponding values) that match the string is set. When set to <b>NULL</b>, all information for the service is set.

### -param bExact [in]

Type: <b>BOOL</b>

Specifies whether the string provided by <i>lpPrefix</i> should be treated as a specific key or a prefix for a set of keys. This parameter is ignored if <i>lpPrefix</i> is set to <b>NULL</b>.

Specify one of the following values.

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
The string specified in <i>lpPrefix</i> represents a specific key. Only that key is set.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The string specified by <i>lpPrefix</i> represents a prefix for a set of keys. All keys (and their values) that have the same prefix is set.

</td>
</tr>
</table>

### -param pvInfo [in]

Type: <b>PVOID</b>

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

## -returns

Type: <b>SCESTATUS</b>

If the function succeeds, it returns SCESTATUS_SUCCESS; otherwise, it returns an error value which can be one of the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges to complete this action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The format is bad.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCESTATUS_PREFIX_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
There is more data than the buffer can hold.

</td>
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
<dt><b>SCESTATUS_NOT_ENOUGH_RESOURCE</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory.

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
<dt><b>SCESTATUS_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified record was not found in the security database.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/scesvc/nc-scesvc-pfsce_query_info">PFSCE_QUERY_INFO</a>



<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_analysis_info">SCESVC_ANALYSIS_INFO</a>



<a href="/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info">SCESVC_CONFIGURATION_INFO</a>
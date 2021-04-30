---
UID: NC:scesvc.PFSCE_LOG_INFO
title: PFSCE_LOG_INFO (scesvc.h)
description: Logs messages to the configuration log file or analysis log file.
helpviewer_keywords: ["PFSCE_LOG_INFO","PFSCE_LOG_INFO callback","PFSCE_LOG_INFO callback function [Security]","SCE_LOG_LEVEL_ALWAYS","SCE_LOG_LEVEL_DEBUG","SCE_LOG_LEVEL_DETAIL","SCE_LOG_LEVEL_ERROR","_config_pfsce_log_info","scesvc/PFSCE_LOG_INFO","security.pfsce_log_info"]
old-location: security\pfsce_log_info.htm
tech.root: security
ms.assetid: 8960b0c0-abde-4ea1-bbe4-7409a848d81b
ms.date: 12/05/2018
ms.keywords: PFSCE_LOG_INFO, PFSCE_LOG_INFO callback, PFSCE_LOG_INFO callback function [Security], SCE_LOG_LEVEL_ALWAYS, SCE_LOG_LEVEL_DEBUG, SCE_LOG_LEVEL_DETAIL, SCE_LOG_LEVEL_ERROR, _config_pfsce_log_info, scesvc/PFSCE_LOG_INFO, security.pfsce_log_info
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
 - PFSCE_LOG_INFO
 - scesvc/PFSCE_LOG_INFO
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
 - PFSCE_LOG_INFO
---

# PFSCE_LOG_INFO callback function


## -description

The <i>PFSCE_LOG_INFO</i> callback function logs messages to the configuration log file or analysis log file.

## -parameters

### -param ErrLevel [in]

Specifies the level of information to log. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCE_LOG_LEVEL_ALWAYS"></a><a id="sce_log_level_always"></a><dl>
<dt><b>SCE_LOG_LEVEL_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
Records all actions in the log file.

</td>
</tr>
<tr>
<td width="40%"><a id="SCE_LOG_LEVEL_ERROR"></a><a id="sce_log_level_error"></a><dl>
<dt><b>SCE_LOG_LEVEL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
Records errors in the log file.

</td>
</tr>
<tr>
<td width="40%"><a id="SCE_LOG_LEVEL_DETAIL"></a><a id="sce_log_level_detail"></a><dl>
<dt><b>SCE_LOG_LEVEL_DETAIL</b></dt>
</dl>
</td>
<td width="60%">
Records detailed information in the log file.

</td>
</tr>
<tr>
<td width="40%"><a id="SCE_LOG_LEVEL_DEBUG"></a><a id="sce_log_level_debug"></a><dl>
<dt><b>SCE_LOG_LEVEL_DEBUG</b></dt>
</dl>
</td>
<td width="60%">
Records debug information in the log file.

</td>
</tr>
</table>

### -param Win32rc [in]

Specifies the Windows result code to log.

### -param pErrFmt [in]

Specifies the result format. This parameter uses the same format conventions as the C library function <b>printf</b>.

### -param unnamedParam1

####### - ... [in]

Variable-length list of arguments specified by <i>pErrFmt</i>. For example, if the string pointed to by <i>pErrFmt</i> is "%d%s%d", <i>pErrFmt</i> is followed by three additional arguments: a <b>DWORD</b>, a string, and another <b>DWORD</b>.

## -returns

If the function succeeds, it returns SCESTATUS_SUCCESS; otherwise, an error code is returned.


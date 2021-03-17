---
UID: NF:werapi.WerAddExcludedApplication
title: WerAddExcludedApplication function (werapi.h)
description: Adds the specified application to the list of applications that are to be excluded from error reporting.
helpviewer_keywords: ["WerAddExcludedApplication","WerAddExcludedApplication function [Windows Error Reporting]","base.weraddexcludedapplication","wer.weraddexcludedapplication","werapi/WerAddExcludedApplication"]
old-location: wer\weraddexcludedapplication.htm
tech.root: wer
ms.assetid: ac1ec373-868f-4634-8658-4253d4f5923a
ms.date: 12/05/2018
ms.keywords: WerAddExcludedApplication, WerAddExcludedApplication function [Windows Error Reporting], base.weraddexcludedapplication, wer.weraddexcludedapplication, werapi/WerAddExcludedApplication
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wer.lib
req.dll: Wer.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WerAddExcludedApplication
 - werapi/WerAddExcludedApplication
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wer.dll
api_name:
 - WerAddExcludedApplication
---

# WerAddExcludedApplication function


## -description

Adds the specified application to the list of applications that are to be excluded from error reporting.

## -parameters

### -param pwzExeName [in]

A pointer to a Unicode string that specifies the name of the executable file for the application, including the file name extension. The maximum length of this path is MAX_PATH characters.

### -param bAllUsers [in]

If this parameter is <b>TRUE</b>, the application name is added to the list of excluded applications for all users. Otherwise, it is only added to the list of excluded applications for the current user.

## -returns

This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The process does not have permissions to update the list in the registry. See the Remarks section for additional information.

</td>
</tr>
</table>

## -remarks

If <i>bAllUsers</i> is <b>TRUE</b>, the list of excluded applications is stored under the HKEY_LOCAL_MACHINE registry hive. The calling process must have permissions to write to the HKLM registry hive.
If <i>bAllUsers</i> is <b>FALSE</b>, the list of excluded applications is stored under the HKEY_CURRENT_USER registry hive.

To remove the application from the list of excluded applications, call the <a href="/windows/desktop/api/werapi/nf-werapi-werremoveexcludedapplication">WerRemoveExcludedApplication</a> function.

## -see-also

<a href="/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="/windows/desktop/api/werapi/nf-werapi-werremoveexcludedapplication">WerRemoveExcludedApplication</a>



<a href="/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>
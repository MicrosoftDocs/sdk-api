---
UID: NF:werapi.WerRemoveExcludedApplication
title: WerRemoveExcludedApplication function (werapi.h)
description: Removes the specified application from the list of applications that are to be excluded from error reporting.
helpviewer_keywords: ["WerRemoveExcludedApplication","WerRemoveExcludedApplication function [Windows Error Reporting]","base.werremoveexcludedapplication","wer.werremoveexcludedapplication","werapi/WerRemoveExcludedApplication"]
old-location: wer\werremoveexcludedapplication.htm
tech.root: wer
ms.assetid: e7bab01b-a09c-4b06-a233-34ed63f75857
ms.date: 12/05/2018
ms.keywords: WerRemoveExcludedApplication, WerRemoveExcludedApplication function [Windows Error Reporting], base.werremoveexcludedapplication, wer.werremoveexcludedapplication, werapi/WerRemoveExcludedApplication
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
 - WerRemoveExcludedApplication
 - werapi/WerRemoveExcludedApplication
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
 - WerRemoveExcludedApplication
---

# WerRemoveExcludedApplication function


## -description

Removes the specified application from the list of applications that are to be excluded from error reporting.

## -parameters

### -param pwzExeName [in]

A pointer to a Unicode string that specifies the name of the executable file for the application, including the file name extension. The maximum length of this path is MAX_PATH characters.

This file must have been excluded using the <a href="/windows/desktop/api/werapi/nf-werapi-weraddexcludedapplication">WerAddExcludedApplication</a> function or **WerRemoveExcludedApplication** fails.

### -param bAllUsers [in]

If this parameter is **TRUE**, the application name is removed from the list of excluded applications for all users. Otherwise, it is only removed from the list of excluded applications for the current user.

## -returns

This function returns **S_OK** on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>**E_ACCESSDENIED**</dt>
</dl>
</td>
<td width="60%">
The process does not have access to update the list in the registry. See the Remarks section for additional information.

</td>
</tr>
</table>

## -remarks

This function removes applications that were added to the excluded applications list using the <a href="/windows/desktop/api/werapi/nf-werapi-weraddexcludedapplication">WerAddExcludedApplication</a> function.

If *bAllUsers* is **TRUE**, the list of excluded applications is stored under the HKEY_LOCAL_MACHINE registry hive. The calling process must have permissions to write to HKLM registry hive.
If *bAllUsers* is **FALSE**, the list of excluded applications is stored under the HKEY_CURRENT_USER registry hive.

## -see-also




<a href="/windows/desktop/api/werapi/nf-werapi-weraddexcludedapplication">WerAddExcludedApplication</a>



[Windows Error Reporting](/windows/desktop/wer)
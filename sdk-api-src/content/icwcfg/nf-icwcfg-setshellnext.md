---
UID: NF:icwcfg.SetShellNext
title: SetShellNext function (icwcfg.h)
description: Sets the ShellNext registry key with the specified value.
helpviewer_keywords: ["SetShellNext","SetShellNext function [Windows API]","icwcfg/SetShellNext","winprog.setshellnext"]
old-location: winprog\setshellnext.htm
tech.root: winprog
ms.assetid: f08753b2-9666-498d-aee4-8eb2c7f0d95b
ms.date: 12/05/2018
ms.keywords: SetShellNext, SetShellNext function [Windows API], icwcfg/SetShellNext, winprog.setshellnext
req.header: icwcfg.h
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
req.lib: 
req.dll: Inetcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetShellNext
 - icwcfg/SetShellNext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Inetcfg.dll
api_name:
 - SetShellNext
---

# SetShellNext function


## -description

<p class="CCE_Message">[This function is available for use in the Windows XP  operating system.  It may be altered or unavailable in subsequent versions.]

Sets the <b>ShellNext</b> registry key with the specified value.

## -parameters

### -param szShellNext [in]

The string value.
The length is expected to be less than or equal to <b>MAX_PATH</b> characters.

## -returns

This function can return one of these values.


This function returns one of the following values.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The call is successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>szShellNext</i> contains a <b>NULL</b> pointer or the string is zero in length.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/icwcfg/nf-icwcfg-checkconnectionwizard">CheckConnectionWizard</a>
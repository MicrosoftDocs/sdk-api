---
UID: NF:userenv.DeriveAppContainerSidFromAppContainerName
title: DeriveAppContainerSidFromAppContainerName function (userenv.h)
description: Gets the SID of the specified profile.
helpviewer_keywords: ["DeriveAppContainerSidFromAppContainerName","DeriveAppContainerSidFromAppContainerName function [Windows Shell]","shell.deriveappcontainersidfromappcontainername","userenv/DeriveAppContainerSidFromAppContainerName"]
old-location: shell\deriveappcontainersidfromappcontainername.htm
tech.root: shell
ms.assetid: 233EFA95-289D-4D55-9D56-0630C015ABC7
ms.date: 12/05/2018
ms.keywords: DeriveAppContainerSidFromAppContainerName, DeriveAppContainerSidFromAppContainerName function [Windows Shell], shell.deriveappcontainersidfromappcontainername, userenv/DeriveAppContainerSidFromAppContainerName
req.header: userenv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Userenv.lib
req.dll: Userenv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DeriveAppContainerSidFromAppContainerName
 - userenv/DeriveAppContainerSidFromAppContainerName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - DeriveAppContainerSidFromAppContainerName
---

# DeriveAppContainerSidFromAppContainerName function


## -description

Gets the SID of the specified profile.

## -parameters

### -param pszAppContainerName [in]

The name of the profile.

### -param ppsidAppContainerSid [out]

The SID for the profile. This buffer must be freed using the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-freesid">FreeSid</a> function.

## -returns

This function can return one of these values.

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszAppContainerName</i> parameter, or the  <i>ppsidAppContainerSid</i> parameter is either <b>NULL</b> or not valid.

</td>
</tr>
</table>
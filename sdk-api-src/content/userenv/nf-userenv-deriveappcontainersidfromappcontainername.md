---
UID: NF:userenv.DeriveAppContainerSidFromAppContainerName
title: DeriveAppContainerSidFromAppContainerName function
author: windows-sdk-content
description: Gets the SID of the specified profile.
old-location: shell\deriveappcontainersidfromappcontainername.htm
tech.root: shell
ms.assetid: 233EFA95-289D-4D55-9D56-0630C015ABC7
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: DeriveAppContainerSidFromAppContainerName, DeriveAppContainerSidFromAppContainerName function [Windows Shell], shell.deriveappcontainersidfromappcontainername, userenv/DeriveAppContainerSidFromAppContainerName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Userenv.dll
api_name:
 - DeriveAppContainerSidFromAppContainerName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeriveAppContainerSidFromAppContainerName function


## -description


Gets the SID of the specified profile.


## -parameters




### -param pszAppContainerName [in]

The name of the profile.


### -param ppsidAppContainerSid [out]

The SID for the profile. This buffer must be freed using the <a href="https://msdn.microsoft.com/1e2098d8-4d1f-4353-97c1-549021a5b3fd">FreeSid</a> function.


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
 




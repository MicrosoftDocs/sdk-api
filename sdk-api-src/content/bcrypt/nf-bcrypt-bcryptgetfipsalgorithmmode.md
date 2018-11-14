---
UID: NF:bcrypt.BCryptGetFipsAlgorithmMode
title: BCryptGetFipsAlgorithmMode function
author: windows-sdk-content
description: Determines whether Federal Information Processing Standard (FIPS) compliance is enabled.
old-location: security\bcryptgetfipsalgorithmmode.htm
tech.root: seccng
ms.assetid: eb7b758d-3466-49fe-8729-a8a059fadcde
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: BCryptGetFipsAlgorithmMode, BCryptGetFipsAlgorithmMode function [Security], bcrypt/BCryptGetFipsAlgorithmMode, security.bcryptgetfipsalgorithmmode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
api_name:
 - BCryptGetFipsAlgorithmMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- BCryptGetFipsAlgorithmMode
: 
---

# BCryptGetFipsAlgorithmMode function


## -description


The <b>BCryptGetFipsAlgorithmMode</b> function determines whether Federal Information Processing Standard (FIPS) compliance is enabled.


## -parameters




### -param pfEnabled [out]

The address of a <b>BOOLEAN</b> variable that receives zero if FIPS compliance is not enabled, or a nonzero value if FIPS compliance is enabled.


## -returns



Returns a status code that indicates the success or failure of the function.


Possible return codes include, but are not limited to, the following.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfEnabled</i> parameter is not valid.

</td>
</tr>
</table>
 




## -remarks



<b>BCryptGetFipsAlgorithmMode</b> can be called either from user mode or kernel mode. Kernel mode callers must be executing at <b>PASSIVE_LEVEL</b> <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">IRQL</a>.




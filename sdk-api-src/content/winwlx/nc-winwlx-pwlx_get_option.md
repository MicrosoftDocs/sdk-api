---
UID: NC:winwlx.PWLX_GET_OPTION
title: PWLX_GET_OPTION
author: windows-sdk-content
description: Called by GINA to retrieve the current value of an option.
old-location: security\wlxgetoption.htm
tech.root: secauthn
ms.assetid: 724477d4-ec56-44bd-801e-23c225bafd03
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PWLX_GET_OPTION, PWLX_GET_OPTION callback, WlxGetOption, WlxGetOption callback function [Security], _gina_wlxgetoption, security.wlxgetoption, winwlx/WlxGetOption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: winwlx.h
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
 - winwlx.h
api_name:
 - WlxGetOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PWLX_GET_OPTION callback function


## -description


<p class="CCE_Message">[The WlxGetOption function is no longer available for use as of Windows Server 2008 and Windows Vista.]

Called by <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> to retrieve the current value of an option.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param hWlx [in]

Specifies the Winlogon handle passed to GINA in the 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> call.


### -param Option [in]

Specifies one of the following options: 





### -param *Value [out]

Returns the current value of the option.


## -returns



The <b>WlxGetOption</b> function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The value of the option was returned in the <i>Value</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Winlogon did not return the value.

</td>
</tr>
</table>
 




## -remarks



In order to access this function, the GINA DLL must use the 
<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a> structure and set the Winlogon version to at least WLX_VERSION_1_3 in its 
<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a> call.




## -see-also




<a href="https://msdn.microsoft.com/47e343b8-ee54-45de-98c6-0ec75b45aa90">WLX_DISPATCH_VERSION_1_3</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>



<a href="https://msdn.microsoft.com/9e7bab30-5cc6-4c55-82e4-d888e1af59ed">WlxNegotiate</a>



<a href="https://msdn.microsoft.com/59f775dd-b3ed-4a57-bec7-fa6ddf267401">WlxSetOption</a>
 

 


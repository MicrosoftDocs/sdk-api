---
UID: NF:winwlx.WlxDisplayStatusMessage
title: WlxDisplayStatusMessage function
author: windows-sdk-content
description: Winlogon calls this function when the GINA DLL should display a message.
old-location: security\wlxdisplaystatusmessage.htm
old-project: SecAuthN
ms.assetid: 07df61ff-f5fa-44ab-b3ca-ed7f4338e471
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: WlxDisplayStatusMessage, WlxDisplayStatusMessage function [Security], _gina_wlxdisplaystatusmessage, security.wlxdisplaystatusmessage, winwlx/WlxDisplayStatusMessage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: ICONINFOEXW, *PICONINFOEXW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxDisplayStatusMessage
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlxDisplayStatusMessage function


## -description


<p class="CCE_Message">[The WlxDisplayStatusMessage function is no longer available for use as of Windows Server 2008 and Windows Vista.]


			The <b>WlxDisplayStatusMessage</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/library/windows/hardware/dn927313">Winlogon</a> calls this function when the GINA DLL should display a message.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


### -param hDesktop [in]

A handle to the desktop where the status message should be displayed.


### -param dwOptions [in]

Specifies display options for the status dialog box. The following options are valid: 




STATUSMSG_OPTION_NOANIMATION

STATUSMSG_OPTION_SETFOREGROUND


### -param pTitle [in]

Pointer to a null-terminated wide character string that specifies the title of the message to be displayed.


### -param pMessage [in]

Pointer to a null-terminated wide character string that specifies the message to be displayed.


## -returns



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
Returns <b>TRUE</b> if the message was displayed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>FALSE</b> if the message was not displayed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 


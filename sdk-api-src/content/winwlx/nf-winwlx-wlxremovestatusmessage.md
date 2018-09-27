---
UID: NF:winwlx.WlxRemoveStatusMessage
title: WlxRemoveStatusMessage function
author: windows-sdk-content
description: Winlogon calls this function to tell the GINA DLL to stop displaying the status message.
old-location: security\wlxremovestatusmessage.htm
tech.root: secauthn
ms.assetid: b8e64f7b-04fc-4dbe-8670-314ff8838ba4
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: WlxRemoveStatusMessage, WlxRemoveStatusMessage function [Security], _gina_wlxremovestatusmessage, security.wlxremovestatusmessage, winwlx/WlxRemoveStatusMessage
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winwlx.h
api_name:
 - WlxRemoveStatusMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlxRemoveStatusMessage function


## -description


<p class="CCE_Message">[The WlxRemoveStatusMessage function is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WlxRemoveStatusMessage</b> function must be implemented by a replacement <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> DLL. <a href="https://msdn.microsoft.com/031c898b-3b4d-4b29-811a-112da37b5e3d">Winlogon</a> calls this function to tell the GINA DLL to stop displaying the status message.
<div class="alert"><b>Note</b>   GINA DLLs are ignored in Windows Vista.</div><div> </div>

## -parameters




### -param pWlxContext [in]

Pointer to the GINA context associated with this window station. The GINA returns this context value when Winlogon calls 
<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a> for this station.


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
Return <b>TRUE</b> if the message was removed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Return <b>FALSE</b> if the message was not removed.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/07df61ff-f5fa-44ab-b3ca-ed7f4338e471">WlxDisplayStatusMessage</a>



<a href="https://msdn.microsoft.com/16208bbe-e697-4e75-8a28-a6d311ecb46c">WlxGetStatusMessage</a>



<a href="https://msdn.microsoft.com/db03f2b3-0719-40be-8a42-04ab7110f711">WlxInitialize</a>
 

 


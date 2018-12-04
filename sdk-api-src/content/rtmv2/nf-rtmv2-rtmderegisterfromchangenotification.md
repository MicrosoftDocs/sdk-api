---
UID: NF:rtmv2.RtmDeregisterFromChangeNotification
title: RtmDeregisterFromChangeNotification function
author: windows-sdk-content
description: The RtmDeregisterFromChangeNotification function unregisters a client from change notification and frees all resources allocated to the notification.
old-location: rras\rtmderegisterfromchangenotification.htm
tech.root: rras
ms.assetid: 489668ce-9226-470d-8306-5ad0546275e7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: RtmDeregisterFromChangeNotification, RtmDeregisterFromChangeNotification function [RAS], _rtmv2ref_rtmderegisterfromchangenotification, rras.rtmderegisterfromchangenotification, rtmv2/RtmDeregisterFromChangeNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rtmv2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rtm.lib
req.dll: Rtm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rtm.dll
api_name:
 - RtmDeregisterFromChangeNotification
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RtmDeregisterFromChangeNotification function


## -description


The 
<b>RtmDeregisterFromChangeNotification</b> function unregisters a client from change notification and frees all resources allocated to the notification.


## -parameters




### -param RtmRegHandle [in]

Handle to the client obtained from a previous call to 
<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>.


### -param NotifyHandle [in]

Handle to the change notification to unregister that is obtained from a previous call to 
<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/b7db8664-2775-4f96-8e5b-5062a8abcfe0">RtmMarkDestForChangeNotification</a>



<a href="https://msdn.microsoft.com/b6e04984-ac92-44a2-a18c-018c6b1b49a9">RtmRegisterForChangeNotification</a>



<a href="https://msdn.microsoft.com/542cb23f-81c2-4b29-b049-ebb5827b1d62">RtmReleaseChangedDests</a>
 

 


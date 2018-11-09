---
UID: NF:npapi.CancelConnectNotify
title: CancelConnectNotify function
author: windows-sdk-content
description: Calls CancelConnectNotify before and after each cancel connection operation (WNetCancelConnection and WNetCancelConnection2).
old-location: security\cancelconnectnotify.htm
tech.root: secauthn
ms.assetid: 94bd969d-f94d-449c-971d-d17fff2c07e1
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: CancelConnectNotify, CancelConnectNotify function [Security], _mnp_cancelconnectnotify, npapi/CancelConnectNotify, security.cancelconnectnotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: npapi.h
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
 - Npapi.h
api_name:
 - CancelConnectNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CancelConnectNotify function


## -description


The <a href="https://msdn.microsoft.com/4c4402e9-7455-4868-978f-3899a8fd86c1">Multiple Provider Router</a> (MPR) calls <b>CancelConnectNotify</b> before and after each cancel connection operation (<a href="https://msdn.microsoft.com/e180d497-5e14-459a-8cf6-5664dfb88419">WNetCancelConnection</a> and 
<a href="https://msdn.microsoft.com/8bb8222f-6ede-4bf4-a6e4-681560cce162">WNetCancelConnection2</a>).


## -parameters




### -param lpNotifyInfo [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/43b31128-da9c-470b-b030-0010b250a291">NOTIFYINFO</a> structure that contains information about the notification.


### -param lpCancelInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/cc4cb0fb-ff7d-4bdc-944c-3bf9b08ea72c">NOTIFYCANCEL</a> structure that contains the cancel connection specific information.


## -returns



If the function succeeds, the function should return WN_SUCCESS.

If the function fails, it should return an error code. This can be any of the error codes specified in 
<a href="https://msdn.microsoft.com/f8e6692f-4824-40fe-a5b3-9843689ea02e">Network Security Return Values</a>.




## -remarks



The <b>CancelConnectNotify</b> function is implemented by applications that need to receive notification from the MPR when a network resource is connected or disconnected. For more information about how to write an application that receives such notifications, see 
<a href="https://msdn.microsoft.com/692eb8f2-1c53-4535-b44d-babb30eecd9c">Receiving Connection Notifications</a>.




## -see-also




<a href="https://msdn.microsoft.com/a061b088-81ca-4276-a0d6-9f1d1282a039">AddConnectNotify</a>
 

 


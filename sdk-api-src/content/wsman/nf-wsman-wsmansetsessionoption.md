---
UID: NF:wsman.WSManSetSessionOption
title: WSManSetSessionOption function
author: windows-sdk-content
description: Sets an extended set of options for the session.
old-location: winrm\wsmansetsessionoption.htm
old-project: WinRM
ms.assetid: e6d21412-49c5-4e04-974d-28e0165ddb69
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSManSetSessionOption, WSManSetSessionOption function [Windows Remote Management], winrm.wsmansetsessionoption, wsman/WSManSetSessionOption
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
req.typenames: WSManSessionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WsmSvc.dll
api_name:
-	WSManSetSessionOption
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManSetSessionOption function


## -description


Sets an extended set of options for the session.


## -parameters




### -param session [in]

Specifies the session handle returned by a <a href="https://msdn.microsoft.com/5123d876-5123-4fa4-8f6f-859a26aad825">WSManCreateSession</a> call.  This parameter cannot be <b>NULL</b>.


### -param option

Specifies the option to be set. This parameter must be set to one of the values in the <a href="https://msdn.microsoft.com/6bfe6936-a9d2-4884-a354-41bd62a2feb0">WSManSessionOption</a> enumeration.


### -param data [in]

A pointer to a <a href="https://msdn.microsoft.com/4ff574d4-04b0-47c3-808f-867d6815bffc">WSMAN_DATA</a> structure that defines the option value.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.




## -remarks



If the <b>WSManSetSessionOption</b> method is called with different values specified for the <i>option</i> parameter, the order of the different options is important. The first  time <b>WSManSetSessionOption</b> is called, the transport is set for the session. If a second call requests a different type of transport, the call will fail.

For example, the second method call will fail if the methods are called in the following order:

<ul>
<li><code>WSManSetSessionOption(WSMAN_OPTION_UNENCRYPTED_MESSAGES)</code></li>
<li><code>WSManSetSessionOption(WSMAN_OPTION_ALLOW_NEGOTIATE_IMPLICIT_CREDENTIALS)</code></li>
</ul>
The first method call sets the transport to HTTP because the <i>option</i> parameter is set to <b>WSMAN_OPTION_UNENCRYPTED_MESSAGES</b>.  The second call fails because the option that was passed is applicable for HTTPS and the transport was set to HTTP by the first message.




---
UID: NF:wsman.WSManInitialize
title: WSManInitialize function
author: windows-driver-content
description: Initializes the Windows Remote Management Client API.
old-location: winrm\wsmaninitialize.htm
old-project: WinRM
ms.assetid: 5aa1f451-0d12-4079-9477-1971fc084df2
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: WSManInitialize, WSManInitialize function [Windows Remote Management], winrm.wsmaninitialize, wsman/WSManInitialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WSManSessionOption
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WsmSvc.dll
api_name:
-	WSManInitialize
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManInitialize function


## -description


Initializes the Windows Remote Management Client API. <b>WSManInitialize</b> can be used by different clients on the same process.


## -parameters




### -param flags

A flag of type <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_0</b> or <b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b>.
The client that will use the disconnect-reconnect functionality should use the 
<b>WSMAN_FLAG_REQUESTED_API_VERSION_1_1</b> flag.


### -param apiHandle [out]

Defines a handle that uniquely identifies the client. This parameter cannot be <b>NULL</b>. When you have finished used the handle, close it by calling the <a href="https://msdn.microsoft.com/1b20ead1-cda0-4449-a454-1e695fe71de6">WSManDeinitialize</a> method.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.




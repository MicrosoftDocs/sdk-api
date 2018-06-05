---
UID: NF:wsman.WSManGetSessionOptionAsDword
title: WSManGetSessionOptionAsDword function
author: windows-sdk-content
description: Gets the value of a session option.
old-location: winrm\wsmangetsessionoptionasdword.htm
old-project: WinRM
ms.assetid: 73ff4a3a-89f7-4362-99fb-7423e3fd853f
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: WSManGetSessionOptionAsDword, WSManGetSessionOptionAsDword function [Windows Remote Management], winrm.wsmangetsessionoptionasdword, wsman/WSManGetSessionOptionAsDword
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
-	WSManGetSessionOptionAsDword
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManGetSessionOptionAsDword function


## -description


Gets the value of a session option.


## -parameters




### -param session [in]

Specifies the handle returned by a <a href="https://msdn.microsoft.com/5123d876-5123-4fa4-8f6f-859a26aad825">WSManCreateSession</a> call.  This parameter cannot be <b>NULL</b>.


### -param option

Specifies the option to get. Not all session options can be retrieved. The options are defined in the <a href="https://msdn.microsoft.com/6bfe6936-a9d2-4884-a354-41bd62a2feb0">WSManSessionOption</a> enumeration.


### -param value [in, out]

Specifies the value of specified session option.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.




---
UID: NF:wsman.WSManDeinitialize
title: WSManDeinitialize function
author: windows-sdk-content
description: Deinitializes the Windows Remote Management client stack.
old-location: winrm\wsmandeinitialize.htm
old-project: winrm
ms.assetid: 1b20ead1-cda0-4449-a454-1e695fe71de6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WSManDeinitialize, WSManDeinitialize function [Windows Remote Management], winrm.wsmandeinitialize, wsman/WSManDeinitialize
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WsmSvc.dll
api_name:
 - WSManDeinitialize
product: Windows
targetos: Windows
req.lib: WsmSvc.lib
req.dll: WsmSvc.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WSManDeinitialize function


## -description


Deinitializes the Windows Remote Management client stack. All operations must be complete before a call to this function will return. This is a synchronous call. It is recommended that all operations are explicitly canceled and that all sessions are closed before calling this function.


## -parameters




### -param apiHandle [in, out, optional]

Specifies the API handle returned by a <a href="https://msdn.microsoft.com/5aa1f451-0d12-4079-9477-1971fc084df2">WSManInitialize</a> call. This parameter cannot be <b>NULL</b>.


### -param flags

Reserved for future use. Must be zero.


## -returns



This method returns zero on success. Otherwise, this method returns an error code.




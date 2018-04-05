---
UID: NF:wdsbp.WdsBpCloseHandle
title: WdsBpCloseHandle function
author: windows-driver-content
description: Closes the specified handle.
old-location: wds\wdsbpclosehandle.htm
old-project: Wds
ms.assetid: b35ec3e2-7dd5-4e17-b657-72bafe91921a
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: WdsBpCloseHandle, WdsBpCloseHandle function [Windows Deployment Services], wds.wdsbpclosehandle, wdsbp/WdsBpCloseHandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdsbp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WAITCHAIN_NODE_INFO, *PWAITCHAIN_NODE_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Wdsbp.dll
api_name:
-	WdsBpCloseHandle
product: Windows
targetos: Windows
req.lib: Wdsbp.lib
req.dll: Wdsbp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsBpCloseHandle function


## -description


Closes the specified handle.


## -parameters




### -param hHandle [in]

A handle to be closed. This can be a handle obtained using the <a href="https://msdn.microsoft.com/dc6007ad-0dd5-477d-a49f-45820aa1b5f6">WdsBpParseInitialize</a> or <a href="https://msdn.microsoft.com/a77cbdf5-9025-4e98-8edd-1b9bae8493e7">WdsBpInitialize</a> functions.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




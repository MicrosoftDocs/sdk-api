---
UID: NF:wnvapi.WnvOpen
title: WnvOpen function (wnvapi.h)
description: Provides a handle to the Windows Network Virtualization (WNV) driver object to be used to request and receive WNV notifications.
helpviewer_keywords: ["WnvOpen","WnvOpen function [Windows Network Virtualization]","wnv.wnvopen","wnvapi/WnvOpen"]
old-location: wnv\wnvopen.htm
tech.root: wnv
ms.assetid: C20BA303-7ECD-4CF3-BB5E-D4509162CD85
ms.date: 12/05/2018
ms.keywords: WnvOpen, WnvOpen function [Windows Network Virtualization], wnv.wnvopen, wnvapi/WnvOpen
req.header: wnvapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.dll: Wnvapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WnvOpen
 - wnvapi/WnvOpen
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wnvapi.dll
api_name:
 - WnvOpen
---

# WnvOpen function


## -description

Provides a handle to the Windows Network Virtualization (WNV) driver object to be used to request and receive WNV notifications.



## -returns

Type: <b>HANDLE</b>

If the function succeeds, it returns the handle to the WNV driver object. If the function fails, it returns <b>NULL</b>.

## -remarks

This handle is used for multiple invocations of the <a href="/previous-versions/windows/desktop/api/wnvapi/nf-wnvapi-wnvrequestnotification">WnvRequestNotification</a> function. When you have finished using the handle, close it by calling the <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.

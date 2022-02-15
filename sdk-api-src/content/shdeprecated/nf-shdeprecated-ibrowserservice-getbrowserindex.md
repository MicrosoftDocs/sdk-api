---
UID: NF:shdeprecated.IBrowserService.GetBrowserIndex
title: IBrowserService::GetBrowserIndex (shdeprecated.h)
description: Deprecated. Retrieves the index of the browser in the window hierarchy.
helpviewer_keywords: ["GetBrowserIndex","GetBrowserIndex method [Windows Shell]","GetBrowserIndex method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetBrowserIndex method","IBrowserService.GetBrowserIndex","IBrowserService::GetBrowserIndex","shdeprecated/IBrowserService::GetBrowserIndex","shell.IBrowserService_GetBrowserIndex","zone_IBrowserService_GetBrowserIndex"]
old-location: shell\IBrowserService_GetBrowserIndex.htm
tech.root: shell
ms.assetid: 293d7641-7858-4aa9-983c-6b25a05930d9
ms.date: 12/05/2018
ms.keywords: GetBrowserIndex, GetBrowserIndex method [Windows Shell], GetBrowserIndex method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetBrowserIndex method, IBrowserService.GetBrowserIndex, IBrowserService::GetBrowserIndex, shdeprecated/IBrowserService::GetBrowserIndex, shell.IBrowserService_GetBrowserIndex, zone_IBrowserService_GetBrowserIndex
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::GetBrowserIndex
 - shdeprecated/IBrowserService::GetBrowserIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.GetBrowserIndex
---

# IBrowserService::GetBrowserIndex


## -description

Deprecated. Retrieves the index of the browser in the window hierarchy.



## -returns

Type: <b>DWORD</b>

The index of the browser. A value of -1 indicates the top frame browser.

## -remarks

The index can be used to find a particular browser window.


---
UID: NF:shdeprecated.IBrowserService.GetBrowserByIndex
title: IBrowserService::GetBrowserByIndex
author: windows-driver-content
description: Deprecated. Retrieves the browser with the given index.
old-location: shell\IBrowserService_GetBrowserByIndex.htm
old-project: shell
ms.assetid: 190bd99d-3921-4d7b-8cf3-c91067d3e1f8
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetBrowserByIndex, GetBrowserByIndex method [Windows Shell], GetBrowserByIndex method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetBrowserByIndex method, IBrowserService.GetBrowserByIndex, IBrowserService::GetBrowserByIndex, shdeprecated/IBrowserService::GetBrowserByIndex, shell.IBrowserService_GetBrowserByIndex, zone_IBrowserService_GetBrowserByIndex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	IBrowserService.GetBrowserByIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetBrowserByIndex


## -description


Deprecated. Retrieves the browser with the given index.


## -parameters




### -param dwID [in]

Type: <b>DWORD</b>

A value of type <b>DWORD</b> that indicates the index of the browser.


### -param ppunk [out]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>**</b>

The address of a pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> that indicates the browser with the given index. The calling application must release this resource when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




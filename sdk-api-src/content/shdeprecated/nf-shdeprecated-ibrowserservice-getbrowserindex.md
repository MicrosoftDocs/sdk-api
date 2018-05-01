---
UID: NF:shdeprecated.IBrowserService.GetBrowserIndex
title: IBrowserService::GetBrowserIndex method
author: windows-driver-content
description: Deprecated. Retrieves the index of the browser in the window hierarchy.
old-location: shell\IBrowserService_GetBrowserIndex.htm
old-project: shell
ms.assetid: 293d7641-7858-4aa9-983c-6b25a05930d9
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetBrowserIndex method [Windows Shell], GetBrowserIndex method [Windows Shell], IBrowserService interface, GetBrowserIndex,IBrowserService.GetBrowserIndex, IBrowserService, IBrowserService interface [Windows Shell], GetBrowserIndex method, IBrowserService::GetBrowserIndex, shdeprecated/IBrowserService::GetBrowserIndex, shell.IBrowserService_GetBrowserIndex, zone_IBrowserService_GetBrowserIndex
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
-	IBrowserService.GetBrowserIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetBrowserIndex method


## -description


Deprecated. Retrieves the index of the browser in the window hierarchy.


## -parameters






## -returns



Type: <b>DWORD</b>

The index of the browser. A value of -1 indicates the top frame browser.




## -remarks



The index can be used to find a particular browser window.




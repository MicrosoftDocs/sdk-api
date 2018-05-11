---
UID: NF:shdeprecated.IBrowserService.GetPalette
title: IBrowserService::GetPalette
author: windows-driver-content
description: Deprecated. Retrieves the browser's palette.
old-location: shell\IBrowserService_GetPalette.htm
old-project: shell
ms.assetid: 039a24d0-8cda-48bf-a10b-baf6d76c808d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetPalette, GetPalette method [Windows Shell], GetPalette method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetPalette method, IBrowserService.GetPalette, IBrowserService::GetPalette, shdeprecated/IBrowserService::GetPalette, shell.IBrowserService_GetPalette, zone_IBrowserService_GetPalette
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
-	IBrowserService.GetPalette
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetPalette


## -description


Deprecated. Retrieves the browser's palette.


## -parameters




### -param hpal [out]

Type: <b>HPALETTE*</b>

A pointer to the browser's palette handle, if one exists.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or E_FAIL if there is no palette.




## -remarks



The calling application should not call <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a> on the palette handle retrieved in <i>hpal</i>.




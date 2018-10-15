---
UID: NF:shdeprecated.IBrowserService.GetTitle
title: IBrowserService::GetTitle
author: windows-sdk-content
description: Deprecated. Retrieves the title of a browser window.
old-location: shell\IBrowserService_GetTitle.htm
tech.root: shell
ms.assetid: e5b514e3-8729-4902-961f-177dc1e77aee
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetTitle, GetTitle method [Windows Shell], GetTitle method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetTitle method, IBrowserService.GetTitle, IBrowserService::GetTitle, shdeprecated/IBrowserService::GetTitle, shell.IBrowserService_GetTitle, zone_IBrowserService_GetTitle
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.GetTitle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetTitle


## -description


Deprecated. Retrieves the title of a browser window.


## -parameters




### -param psv [in]

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> that represents the browser's current view.


### -param pszName [out]

Type: <b>LPWSTR</b>

A pointer to a buffer that receives the title.


### -param cchName [in]

Type: <b>DWORD</b>

The size, in characters, of the buffer pointed to by <i>pszName</i>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




---
UID: NF:shdeprecated.IBrowserService.SetReferrer
title: IBrowserService::SetReferrer
author: windows-sdk-content
description: Deprecated. Sets the pointer to an item identifier list (PIDL) used for zone checking when creating a new window.
old-location: shell\IBrowserService_SetReferrer.htm
tech.root: shell
ms.assetid: 6458f28c-4eab-45dc-bc99-24e5f9ea3553
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IBrowserService interface [Windows Shell],SetReferrer method, IBrowserService.SetReferrer, IBrowserService::SetReferrer, SetReferrer, SetReferrer method [Windows Shell], SetReferrer method [Windows Shell],IBrowserService interface, shdeprecated/IBrowserService::SetReferrer, shell.IBrowserService_SetReferrer, zone_IBrowserService_SetReferrer
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
 - IBrowserService.SetReferrer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::SetReferrer


## -description


Deprecated. Sets the pointer to an item identifier list (PIDL) used for zone checking when creating a new window.


## -parameters




### -param pidl [in]

Type: <b>LPITEMIDLIST</b>

A pointer to the <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure (PIDL) used for zone checking.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




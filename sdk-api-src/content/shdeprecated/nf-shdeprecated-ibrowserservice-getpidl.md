---
UID: NF:shdeprecated.IBrowserService.GetPidl
title: IBrowserService::GetPidl
author: windows-sdk-content
description: Deprecated. Retrieves a copy of the current pointer to an item identifier list (PIDL).
old-location: shell\IBrowserService_GetPidl.htm
tech.root: shell
ms.assetid: 49104b30-85c0-4adf-acfc-a06b5c4bbdef
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetPidl, GetPidl method [Windows Shell], GetPidl method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetPidl method, IBrowserService.GetPidl, IBrowserService::GetPidl, shdeprecated/IBrowserService::GetPidl, shell.IBrowserService_GetPidl, zone_IBrowserService_GetPidl
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
 - IBrowserService.GetPidl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetPidl


## -description


Deprecated. Retrieves a copy of the current pointer to an item identifier list (PIDL).


## -parameters




### -param ppidl [out]

Type: <b>LPITEMIDLIST*</b>

A pointer to the current PIDL.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The calling application is responsible for freeing the PIDL by calling <a href="https://msdn.microsoft.com/3457f36e-fdfd-44a4-90ca-a86f00bc9f36">ILFree</a> when the PIDL is no longer needed.




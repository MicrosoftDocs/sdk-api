---
UID: NF:shdeprecated.IBrowserService.DisplayParseError
title: IBrowserService::DisplayParseError (shdeprecated.h)
author: windows-sdk-content
description: Deprecated. Displays a URL that failed to be successfully parsed by IBrowserService::IEParseDisplayName.
old-location: shell\IBrowserService_DisplayParseError.htm
tech.root: shell
ms.assetid: 966fec07-6a67-435a-8908-67999afce9f0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DisplayParseError, DisplayParseError method [Windows Shell], DisplayParseError method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],DisplayParseError method, IBrowserService.DisplayParseError, IBrowserService::DisplayParseError, shdeprecated/IBrowserService::DisplayParseError, shell.IBrowserService_DisplayParseError, zone_IBrowserService_DisplayParseError
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
 - IBrowserService.DisplayParseError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::DisplayParseError


## -description


Deprecated. Displays a URL that failed to be successfully parsed by <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IBrowserService::IEParseDisplayName</a>.


## -parameters




### -param hres [in]

Type: <b>HRESULT</b>

An <b>HRESULT</b> returned by <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IBrowserService::IEParseDisplayName</a>. If this parameter is a success code, E_OUTOFMEMORY, or HRESULT_FROM_WIN32(ERROR_CANCELLED), this method does nothing.


### -param pwszPath [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the URL that failed to parse. This method displays the failed URL in an error dialog box.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>HRESULT</b> returned by <a href="https://msdn.microsoft.com/02f5a6cb-2f90-4613-80cd-1e8a47bb32c2">IBrowserService::IEParseDisplayName</a> can be passed to <b>IBrowserService::DisplayParseError</b> without first checking for success or failure.
      




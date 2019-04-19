---
UID: NF:shdeprecated.IBrowserService2.GetBaseBrowserData
title: IBrowserService2::GetBaseBrowserData (shdeprecated.h)
author: windows-sdk-content
description: Deprecated. Gets a read-only structure containing the protected elements owned by the base class, for the purpose of determining state.
old-location: shell\IBrowserService2_GetBaseBrowserData.htm
tech.root: shell
ms.assetid: 60a9bbd1-5c11-4c6a-bae2-b85979ab8bda
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetBaseBrowserData, GetBaseBrowserData method [Windows Shell], GetBaseBrowserData method [Windows Shell],IBrowserService2 interface, IBrowserService2 interface [Windows Shell],GetBaseBrowserData method, IBrowserService2.GetBaseBrowserData, IBrowserService2::GetBaseBrowserData, shdeprecated/IBrowserService2::GetBaseBrowserData, shell.IBrowserService2_GetBaseBrowserData, zone_IBrowserService2_GetBaseBrowserData
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IBrowserService2.GetBaseBrowserData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
---

# IBrowserService2::GetBaseBrowserData


## -description


Deprecated. Gets a read-only structure containing the protected elements owned by the base class, for the purpose of determining state.
        


## -parameters




### -param pbbd [in, out]

Type: <b>LPCBASEBROWSERDATA*</b>

A pointer to a <a href="https://msdn.microsoft.com/d56e42e8-a556-4470-82d9-466edd84214f">BASEBROWSERDATA</a> structure that receives the read-only state of the base browser.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is used as an optimization to access the internal state of the base browser. The state should be updated only by the base browser.




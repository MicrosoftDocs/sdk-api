---
UID: NF:shdeprecated.IBrowserService2._LoadToolbars
title: IBrowserService2::_LoadToolbars
author: windows-sdk-content
description: Deprecated. Loads the saved state of the browser's toolbars.
old-location: shell\IBrowserService2__LoadToolbars.htm
old-project: shell
ms.assetid: b3dd5b22-8834-4601-b91b-d5c4ded01549
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_LoadToolbars method, IBrowserService2._LoadToolbars, IBrowserService2::_LoadToolbars, _LoadToolbars, _LoadToolbars method [Windows Shell], _LoadToolbars method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_LoadToolbars, shell.IBrowserService2__LoadToolbars, zone_IBrowserService2__LoadToolbars
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2._LoadToolbars
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_LoadToolbars


## -description


Deprecated. Loads the saved state of the browser's toolbars.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> from which to load the state  of the browser's toolbars.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the derived class.




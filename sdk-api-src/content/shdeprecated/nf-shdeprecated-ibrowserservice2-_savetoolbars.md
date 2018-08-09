---
UID: NF:shdeprecated.IBrowserService2._SaveToolbars
title: IBrowserService2::_SaveToolbars
author: windows-sdk-content
description: Deprecated. Saves the state of browser toolbars.
old-location: shell\IBrowserService2__SaveToolbars.htm
old-project: shell
ms.assetid: 8d05ed3d-13a3-49a2-8248-9976bc492b0f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_SaveToolbars method, IBrowserService2._SaveToolbars, IBrowserService2::_SaveToolbars, _SaveToolbars, _SaveToolbars method [Windows Shell], _SaveToolbars method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_SaveToolbars, shell.IBrowserService2__SaveToolbars, zone_IBrowserService2__SaveToolbars
ms.prod: windows
ms.technology: windows-sdk
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
 - IBrowserService2._SaveToolbars
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_SaveToolbars


## -description


Deprecated. Saves the state of browser toolbars.


## -parameters




### -param pstm [in]

Type: <b><a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> used to store the browser toolbar's state.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by the derived class.




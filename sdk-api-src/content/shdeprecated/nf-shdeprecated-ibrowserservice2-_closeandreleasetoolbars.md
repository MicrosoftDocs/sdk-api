---
UID: NF:shdeprecated.IBrowserService2._CloseAndReleaseToolbars
title: IBrowserService2::_CloseAndReleaseToolbars
author: windows-sdk-content
description: Deprecated. Requests the closing of the browser toolbars hosted by the derived class.
old-location: shell\IBrowserService2__CloseAndReleaseToolbars.htm
old-project: shell
ms.assetid: 2028fbc6-41e1-4d98-9149-7de6458c5446
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_CloseAndReleaseToolbars method, IBrowserService2._CloseAndReleaseToolbars, IBrowserService2::_CloseAndReleaseToolbars, _CloseAndReleaseToolbars, _CloseAndReleaseToolbars method [Windows Shell], _CloseAndReleaseToolbars method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_CloseAndReleaseToolbars, shell.IBrowserService2__CloseAndReleaseToolbars, zone_IBrowserService2__CloseAndReleaseToolbars
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
 - IBrowserService2._CloseAndReleaseToolbars
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_CloseAndReleaseToolbars


## -description


Deprecated. Requests the closing of the browser toolbars hosted by the derived class.


## -parameters




### -param fClose [in]

Type: <b>BOOL</b>

<b>TRUE</b> to close the toolbar through <a href="https://msdn.microsoft.com/29e57436-cc8f-46e8-bc1a-b44bd803c4a8">IDockingWindow::CloseDW</a>; <b>FALSE</b> to release the toolbar.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




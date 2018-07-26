---
UID: NF:shdeprecated.IBrowserService2._UIActivateView
title: IBrowserService2::_UIActivateView
author: windows-sdk-content
description: Deprecated. Allows a derived class to request that the base class update the browser view.
old-location: shell\IBrowserService2__UIActivateView.htm
old-project: shell
ms.assetid: 9c8439f8-5931-4aca-8085-2707b6f964f0
ms.author: windowssdkdev
ms.date: 07/20/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_UIActivateView method, IBrowserService2._UIActivateView, IBrowserService2::_UIActivateView, _UIActivateView, _UIActivateView method [Windows Shell], _UIActivateView method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_UIActivateView, shell.IBrowserService2__UIActivateView, zone_IBrowserService2__UIActivateView
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
 - IBrowserService2._UIActivateView
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_UIActivateView


## -description


Deprecated. Allows a derived class to request that the base class update the browser view.


## -parameters




### -param uState [in]

Type: <b>UINT</b>

A member of the <a href="https://msdn.microsoft.com/04cb4259-4d16-44d0-8186-bce21ceab887">SVUIA_STATUS</a> enumeration declaring the browser view's state value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




---
UID: NF:shdeprecated.IBrowserService2._OnFocusChange
title: IBrowserService2::_OnFocusChange
author: windows-sdk-content
description: Deprecated. Coordinates focus between the base and the derived class when the focus shifts between the derived class's browser toolbars and its view.
old-location: shell\IBrowserService2__OnFocusChange.htm
old-project: shell
ms.assetid: 724b6f35-c419-4b67-bffd-c509e54715d0
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_OnFocusChange method, IBrowserService2._OnFocusChange, IBrowserService2::_OnFocusChange, _OnFocusChange, _OnFocusChange method [Windows Shell], _OnFocusChange method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_OnFocusChange, shell.IBrowserService2__OnFocusChange, zone_IBrowserService2__OnFocusChange
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
 - IBrowserService2._OnFocusChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_OnFocusChange


## -description


Deprecated. Coordinates focus between the base and the derived class when the focus shifts between the derived class's browser toolbars and its view.


## -parameters




### -param itb [in]

Type: <b>UINT</b>

The ID of the toolbar gaining focus, or ITB_VIEW if the view is gaining focus.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




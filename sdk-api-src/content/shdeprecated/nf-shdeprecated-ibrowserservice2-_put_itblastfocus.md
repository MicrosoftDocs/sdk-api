---
UID: NF:shdeprecated.IBrowserService2._put_itbLastFocus
title: IBrowserService2::_put_itbLastFocus
author: windows-sdk-content
description: Deprecated. Sets the last toolbar or the last view with focus.
old-location: shell\IBrowserService2__put_itbLastFocus.htm
old-project: shell
ms.assetid: 08b67fad-1c9d-46b6-81dd-d77721448bc6
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IBrowserService2 interface [Windows Shell],_put_itbLastFocus method, IBrowserService2._put_itbLastFocus, IBrowserService2::_put_itbLastFocus, _put_itbLastFocus, _put_itbLastFocus method [Windows Shell], _put_itbLastFocus method [Windows Shell],IBrowserService2 interface, shdeprecated/IBrowserService2::_put_itbLastFocus, shell.IBrowserService2__put_itbLastFocus, zone_IBrowserService2__put_itbLastFocus
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
 - IBrowserService2._put_itbLastFocus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::_put_itbLastFocus


## -description


Deprecated. Sets the last toolbar or the last view with focus.


## -parameters




### -param itbLastFocus [in]

Type: <b>UINT</b>

The index of the last toolbar with focus. Set this parameter to ITB_VIEW to indicate that the view had the last focus.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




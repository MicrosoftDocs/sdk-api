---
UID: NF:shdeprecated.IBrowserService2.v_ShowHideChildWindows
title: IBrowserService2::v_ShowHideChildWindows
author: windows-sdk-content
description: Deprecated. Allows a derived class to update its child windows after a sizing event.
old-location: shell\IBrowserService2_v_ShowHideChildWindows.htm
tech.root: shell
ms.assetid: b97116f7-d42e-4619-bc5b-0a55ac012f0c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IBrowserService2 interface [Windows Shell],v_ShowHideChildWindows method, IBrowserService2.v_ShowHideChildWindows, IBrowserService2::v_ShowHideChildWindows, shdeprecated/IBrowserService2::v_ShowHideChildWindows, shell.IBrowserService2_v_ShowHideChildWindows, v_ShowHideChildWindows, v_ShowHideChildWindows method [Windows Shell], v_ShowHideChildWindows method [Windows Shell],IBrowserService2 interface, zone_IBrowserService2_v_ShowHideChildWindows
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IBrowserService2.v_ShowHideChildWindows
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- shdeprecated.h
: 
- IBrowserService2.v_ShowHideChildWindows
: 
req.product: Internet Explorer 5.0
---

# IBrowserService2::v_ShowHideChildWindows


## -description


Deprecated. Allows a derived class to update its child windows after a sizing event.


## -parameters




### -param fChildOnly [in]

Type: <b>BOOL</b>

A value of type <b>BOOL</b> that indicates whether child windows should be shown or hidden.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




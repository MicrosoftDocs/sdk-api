---
UID: NF:shdeprecated.IBrowserService2.v_ShowHideChildWindows
title: IBrowserService2::v_ShowHideChildWindows (shdeprecated.h)
description: Deprecated. Allows a derived class to update its child windows after a sizing event.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","v_ShowHideChildWindows method","IBrowserService2.v_ShowHideChildWindows","IBrowserService2::v_ShowHideChildWindows","shdeprecated/IBrowserService2::v_ShowHideChildWindows","shell.IBrowserService2_v_ShowHideChildWindows","v_ShowHideChildWindows","v_ShowHideChildWindows method [Windows Shell]","v_ShowHideChildWindows method [Windows Shell]","IBrowserService2 interface","zone_IBrowserService2_v_ShowHideChildWindows"]
old-location: shell\IBrowserService2_v_ShowHideChildWindows.htm
tech.root: shell
ms.assetid: b97116f7-d42e-4619-bc5b-0a55ac012f0c
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],v_ShowHideChildWindows method, IBrowserService2.v_ShowHideChildWindows, IBrowserService2::v_ShowHideChildWindows, shdeprecated/IBrowserService2::v_ShowHideChildWindows, shell.IBrowserService2_v_ShowHideChildWindows, v_ShowHideChildWindows, v_ShowHideChildWindows method [Windows Shell], v_ShowHideChildWindows method [Windows Shell],IBrowserService2 interface, zone_IBrowserService2_v_ShowHideChildWindows
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService2::v_ShowHideChildWindows
 - shdeprecated/IBrowserService2::v_ShowHideChildWindows
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService2.v_ShowHideChildWindows
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.


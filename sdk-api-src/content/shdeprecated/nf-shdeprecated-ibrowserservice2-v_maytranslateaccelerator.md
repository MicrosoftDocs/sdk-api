---
UID: NF:shdeprecated.IBrowserService2.v_MayTranslateAccelerator
title: IBrowserService2::v_MayTranslateAccelerator (shdeprecated.h)
description: Deprecated. Called by a derived class to instruct the base class to proceed with the translation of keyboard mnemonics.
helpviewer_keywords: ["IBrowserService2 interface [Windows Shell]","v_MayTranslateAccelerator method","IBrowserService2.v_MayTranslateAccelerator","IBrowserService2::v_MayTranslateAccelerator","shdeprecated/IBrowserService2::v_MayTranslateAccelerator","shell.IBrowserService2_v_MayTranslateAccelerator","v_MayTranslateAccelerator","v_MayTranslateAccelerator method [Windows Shell]","v_MayTranslateAccelerator method [Windows Shell]","IBrowserService2 interface","zone_IBrowserService2_v_MayTranslateAccelerator"]
old-location: shell\IBrowserService2_v_MayTranslateAccelerator.htm
tech.root: shell
ms.assetid: 99dc3bce-c661-4233-8457-0ce29e02c270
ms.date: 12/05/2018
ms.keywords: IBrowserService2 interface [Windows Shell],v_MayTranslateAccelerator method, IBrowserService2.v_MayTranslateAccelerator, IBrowserService2::v_MayTranslateAccelerator, shdeprecated/IBrowserService2::v_MayTranslateAccelerator, shell.IBrowserService2_v_MayTranslateAccelerator, v_MayTranslateAccelerator, v_MayTranslateAccelerator method [Windows Shell], v_MayTranslateAccelerator method [Windows Shell],IBrowserService2 interface, zone_IBrowserService2_v_MayTranslateAccelerator
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
 - IBrowserService2::v_MayTranslateAccelerator
 - shdeprecated/IBrowserService2::v_MayTranslateAccelerator
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
 - IBrowserService2.v_MayTranslateAccelerator
---

# IBrowserService2::v_MayTranslateAccelerator


## -description

Deprecated. Called by a derived class to instruct the base class to proceed with the translation of keyboard mnemonics.

## -parameters

### -param pmsg [in]

Type: <b><a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a>*</b>

A pointer to a <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> that contains the keystroke message.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
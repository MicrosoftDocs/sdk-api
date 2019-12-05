---
UID: NF:oleauto.RevokeActiveObject
title: RevokeActiveObject function (oleauto.h)
description: Ends an object's status as active.
old-location: automat\revokeactiveobject.htm
tech.root: automat
ms.assetid: 47e7b47b-dddc-445d-918f-02b1b6a37075
ms.date: 12/05/2018
ms.keywords: RevokeActiveObject, RevokeActiveObject function [Automation], _oa96_RevokeActiveObject, automat.revokeactiveobject, oleauto/RevokeActiveObject
ms.topic: function
f1_keywords:
- oleauto/RevokeActiveObject
dev_langs:
- c++
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- RevokeActiveObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RevokeActiveObject function


## -description


Ends an object's status as active.


## -parameters




### -param dwRegister [in]

A handle previously returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-registeractiveobject">RegisterActiveObject</a>.




### -param pvReserved

Reserved for future use. Must be null.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




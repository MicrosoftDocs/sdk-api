---
UID: NN:shdeprecated.ITravelEntry
title: ITravelEntry (shdeprecated.h)
description: Deprecated. Exposes methods to identify, invoke, and update an individual item in the browser's travel history.
helpviewer_keywords: ["ITravelEntry","ITravelEntry interface [Windows Shell]","ITravelEntry interface [Windows Shell]","described","shdeprecated/ITravelEntry","shell.ITravelEntry","zone_ITravelEntry"]
old-location: shell\ITravelEntry.htm
tech.root: shell
ms.assetid: b8a5d532-c1fd-4302-b983-cc9a74270321
ms.date: 12/05/2018
ms.keywords: ITravelEntry, ITravelEntry interface [Windows Shell], ITravelEntry interface [Windows Shell],described, shdeprecated/ITravelEntry, shell.ITravelEntry, zone_ITravelEntry
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - ITravelEntry
 - shdeprecated/ITravelEntry
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
 - ITravelEntry
---

# ITravelEntry interface


## -description

Deprecated. Exposes methods to identify, invoke, and update an individual item in the browser's travel history.

## -inheritance

The <b>ITravelEntry</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITravelEntry</b> also has these types of members:

## -remarks

Travel entries represented by <b>ITravelEntry</b> are created and maintained internally by the travel log (<a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>). Calling applications rarely use <b>ITravelEntry</b> directly.

<div class="alert"><b>Note</b>  <b>ITravelEntry</b> may not be supported in versions of Windows later than Windows XP.</div>
<div> </div>

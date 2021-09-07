---
UID: NF:shdeprecated.ITravelEntry.Update
title: ITravelEntry::Update (shdeprecated.h)
description: Deprecated. Updates the travel entry.
helpviewer_keywords: ["FALSE","ITravelEntry interface [Windows Shell]","Update method","ITravelEntry.Update","ITravelEntry::Update","TRUE","Update","Update method [Windows Shell]","Update method [Windows Shell]","ITravelEntry interface","shdeprecated/ITravelEntry::Update","shell.ITravelEntry_Update","zone_ITravelEntry_Update"]
old-location: shell\ITravelEntry_Update.htm
tech.root: shell
ms.assetid: 49861eb7-0e8e-41d9-b9b7-3b9bd35d0e52
ms.date: 12/05/2018
ms.keywords: FALSE, ITravelEntry interface [Windows Shell],Update method, ITravelEntry.Update, ITravelEntry::Update, TRUE, Update, Update method [Windows Shell], Update method [Windows Shell],ITravelEntry interface, shdeprecated/ITravelEntry::Update, shell.ITravelEntry_Update, zone_ITravelEntry_Update
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
 - ITravelEntry::Update
 - shdeprecated/ITravelEntry::Update
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
 - ITravelEntry.Update
---

# ITravelEntry::Update


## -description

Deprecated. Updates the travel entry.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the browser or frame within which the travel operation generating the entry is taking place.

### -param fIsLocalAnchor [in]

Type: <b>BOOL</b>

The value specifying whether the new entry is a local anchor.



#### TRUE

The entry is an anchor link within the same page.



#### FALSE

The entry is another page or an anchor on another page.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
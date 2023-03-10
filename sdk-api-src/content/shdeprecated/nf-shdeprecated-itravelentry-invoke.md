---
UID: NF:shdeprecated.ITravelEntry.Invoke
title: ITravelEntry::Invoke (shdeprecated.h)
description: Deprecated. Invokes the travel entry, navigating to that page.
helpviewer_keywords: ["ITravelEntry interface [Windows Shell]","Invoke method","ITravelEntry.Invoke","ITravelEntry::Invoke","Invoke","Invoke method [Windows Shell]","Invoke method [Windows Shell]","ITravelEntry interface","shdeprecated/ITravelEntry::Invoke","shell.ITravelEntry_Invoke","zone_ITravelEntry_Invoke"]
old-location: shell\ITravelEntry_Invoke.htm
tech.root: shell
ms.assetid: 21af8d98-f7b6-4204-b855-a4789492a882
ms.date: 12/05/2018
ms.keywords: ITravelEntry interface [Windows Shell],Invoke method, ITravelEntry.Invoke, ITravelEntry::Invoke, Invoke, Invoke method [Windows Shell], Invoke method [Windows Shell],ITravelEntry interface, shdeprecated/ITravelEntry::Invoke, shell.ITravelEntry_Invoke, zone_ITravelEntry_Invoke
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
 - ITravelEntry::Invoke
 - shdeprecated/ITravelEntry::Invoke
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
 - ITravelEntry.Invoke
---

# ITravelEntry::Invoke


## -description

Deprecated. Invokes the travel entry, navigating to that page.

## -parameters

### -param punk [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the browser or frame within which the travel operation generating the entry is taking place.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
---
UID: NF:shdeprecated.ITravelEntry.Update
title: ITravelEntry::Update
author: windows-sdk-content
description: Deprecated. Updates the travel entry.
old-location: shell\ITravelEntry_Update.htm
old-project: shell
ms.assetid: 49861eb7-0e8e-41d9-b9b7-3b9bd35d0e52
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: FALSE, ITravelEntry interface [Windows Shell],Update method, ITravelEntry.Update, ITravelEntry::Update, TRUE, Update, Update method [Windows Shell], Update method [Windows Shell],ITravelEntry interface, shdeprecated/ITravelEntry::Update, shell.ITravelEntry_Update, zone_ITravelEntry_Update
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - ITravelEntry.Update
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# ITravelEntry::Update


## -description


Deprecated. Updates the travel entry.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> representing the browser or frame within which the travel operation generating the entry is taking place.


### -param fIsLocalAnchor [in]

Type: <b>BOOL</b>

The value specifying whether the new entry is a local anchor.



#### TRUE

The entry is an anchor link within the same page.



#### FALSE

The entry is another page or an anchor on another page.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




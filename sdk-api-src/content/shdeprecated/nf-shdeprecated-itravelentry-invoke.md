---
UID: NF:shdeprecated.ITravelEntry.Invoke
title: ITravelEntry::Invoke
author: windows-sdk-content
description: Deprecated. Invokes the travel entry, navigating to that page.
old-location: shell\ITravelEntry_Invoke.htm
old-project: shell
ms.assetid: 21af8d98-f7b6-4204-b855-a4789492a882
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ITravelEntry interface [Windows Shell],Invoke method, ITravelEntry.Invoke, ITravelEntry::Invoke, Invoke, Invoke method [Windows Shell], Invoke method [Windows Shell],ITravelEntry interface, shdeprecated/ITravelEntry::Invoke, shell.ITravelEntry_Invoke, zone_ITravelEntry_Invoke
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	ITravelEntry.Invoke
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# ITravelEntry::Invoke


## -description


Deprecated. Invokes the travel entry, navigating to that page.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> representing the browser or frame within which the travel operation generating the entry is taking place.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




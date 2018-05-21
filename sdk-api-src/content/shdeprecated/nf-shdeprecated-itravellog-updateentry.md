---
UID: NF:shdeprecated.ITravelLog.UpdateEntry
title: ITravelLog::UpdateEntry
author: windows-driver-content
description: Deprecated. Saves the browser state of the current entry in preparation for a pending navigation.
old-location: shell\ITravelLog_UpdateEntry.htm
old-project: shell
ms.assetid: 63fe398d-c0e8-4350-9b57-fe9f11e24e47
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: FALSE, ITravelLog interface [Windows Shell],UpdateEntry method, ITravelLog.UpdateEntry, ITravelLog::UpdateEntry, TRUE, UpdateEntry, UpdateEntry method [Windows Shell], UpdateEntry method [Windows Shell],ITravelLog interface, shdeprecated/ITravelLog::UpdateEntry, shell.ITravelLog_UpdateEntry, zone_ITravelLog_UpdateEntry
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BNSTATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shdeprecated.h
api_name:
-	ITravelLog.UpdateEntry
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# ITravelLog::UpdateEntry


## -description


Deprecated. Saves the browser state of the current entry in preparation for a pending navigation.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> that represents the nearest browser or frame within which the travel generating the log is taking place.


### -param fIsLocalAnchor [in]

Type: <b>BOOL</b>

A value specifying whether the new entry is a local anchor.



#### TRUE

The entry is an anchor link within the same page.



#### FALSE

The entry is another page or an anchor on another page.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




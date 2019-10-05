---
UID: NF:shdeprecated.ITravelLog.AddEntry
title: ITravelLog::AddEntry (shdeprecated.h)
author: windows-sdk-content
description: Deprecated. Adds a new entry for a pending navigation to the travel log.
old-location: shell\ITravelLog_AddEntry.htm
tech.root: shell
ms.assetid: f83c1cb1-3cc5-413c-826b-ff4971cd4598
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddEntry, AddEntry method [Windows Shell], AddEntry method [Windows Shell],ITravelLog interface, FALSE, ITravelLog interface [Windows Shell],AddEntry method, ITravelLog.AddEntry, ITravelLog::AddEntry, TRUE, shdeprecated/ITravelLog::AddEntry, shell.ITravelLog_AddEntry, zone_ITravelLog_AddEntry
ms.topic: method
f1_keywords: 
 - "shdeprecated/ITravelLog.AddEntry"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - ITravelLog.AddEntry
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
---

# ITravelLog::AddEntry


## -description


Deprecated. Adds a new entry for a pending navigation to the travel log.


## -parameters




### -param punk [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> representing the nearest browser or frame within which the travel generating the log is taking place.


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




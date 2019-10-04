---
UID: NF:dwrite_3.IDWriteFontCollection3.GetExpirationEvent
title: IDWriteFontCollection3::GetExpirationEvent
author: windows-sdk-content
description: Retrieves the expiration event for the font set, if any. The expiration event is set on a system font set object if it is out of date due to fonts being installed, uninstalled, or updated.
tech.root: DirectWrite
ms.author: windowssdkdev
ms.date: 09/12/2019
ms.keywords: IDWriteFontCollection3 interface [Direct Write],GetExpirationEvent method, IDWriteFontCollection3.GetExpirationEvent, IDWriteFontCollection3::GetExpirationEvent, GetExpirationEvent, GetExpirationEvent method [Direct Write], GetExpirationEvent method [Direct Write],IDWriteFontCollection3 interface, directwrite.idwritefontcollection3_getexpirationevent, dwrite_3/IDWriteFontCollection3::GetExpirationEvent
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFontCollection3.GetExpirationEvent"
dev_langs:
 - c++
req.construct-type: function
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontCollection3::GetExpirationEvent
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the expiration event for the font set, if any. The expiration event is set on a system font set object if it is out of date due to fonts being installed, uninstalled, or updated. You should handle the event by getting a new system font set.

## -returns

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

An event handle, if called on the system font set, or `nullptr` if called on a custom font set.

## -remarks

You mustn't call **CloseHandle** on the returned event handle. The handle is owned by the font set object, and it remains valid as long as you hold a reference to the font set. You can wait on the returned event, or use [RegisterWaitForSingleObject](/windows/win32/api/winbase/nf-winbase-registerwaitforsingleobject) to request a callback when the event is set.

## -see-also

---
UID: NF:dwrite_3.IDWriteFontCollection3.GetExpirationEvent
title: IDWriteFontCollection3::GetExpirationEvent
description: Retrieves the expiration event for the font set, if any. The expiration event is set on a system font set object if it is out of date due to fonts being installed, uninstalled, or updated. (IDWriteFontCollection3::GetExpirationEvent)
helpviewer_keywords: ["IDWriteFontCollection3 interface [Direct Write]","GetExpirationEvent method","IDWriteFontCollection3.GetExpirationEvent","IDWriteFontCollection3::GetExpirationEvent","GetExpirationEvent","GetExpirationEvent method [Direct Write]","GetExpirationEvent method [Direct Write]","IDWriteFontCollection3 interface","directwrite.idwritefontcollection3_getexpirationevent","dwrite_3/IDWriteFontCollection3::GetExpirationEvent"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFontCollection3 interface [Direct Write],GetExpirationEvent method, IDWriteFontCollection3.GetExpirationEvent, IDWriteFontCollection3::GetExpirationEvent, GetExpirationEvent, GetExpirationEvent method [Direct Write], GetExpirationEvent method [Direct Write],IDWriteFontCollection3 interface, directwrite.idwritefontcollection3_getexpirationevent, dwrite_3/IDWriteFontCollection3::GetExpirationEvent
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 17134
req.target-min-winversvr: Windows 10 Build 17134
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IDWriteFontCollection3::GetExpirationEvent
 - dwrite_3/IDWriteFontCollection3::GetExpirationEvent
dev_langs:
 - c++
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
---

## -description

Retrieves the expiration event for the font set, if any. The expiration event is set on a system font set object if it is out of date due to fonts being installed, uninstalled, or updated. You should handle the event by getting a new system font set.



## -returns

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

An event handle, if called on the system font set, or `nullptr` if called on a custom font set.

## -remarks

You mustn't call **CloseHandle** on the returned event handle. The handle is owned by the font set object, and it remains valid as long as you hold a reference to the font set. You can wait on the returned event, or use [RegisterWaitForSingleObject](../winbase/nf-winbase-registerwaitforsingleobject.md) to request a callback when the event is set.

## -see-also

---
UID: NF:dwrite_3.IDWriteFontSet2.GetExpirationEvent
title: IDWriteFontSet2::GetExpirationEvent
description: Retrieves the expiration event for the font set, if any. The expiration event is set on a system font set object if it is out of date due to fonts being installed, uninstalled, or updated. (IDWriteFontSet2::GetExpirationEvent)
helpviewer_keywords: ["IDWriteFontSet2 interface [Direct Write]","GetExpirationEvent method","IDWriteFontSet2.GetExpirationEvent","IDWriteFontSet2::GetExpirationEvent","GetExpirationEvent","GetExpirationEvent method [Direct Write]","GetExpirationEvent method [Direct Write]","IDWriteFontSet2 interface","directwrite.idwritefontset2_getexpirationevent","dwrite_3/IDWriteFontSet2::GetExpirationEvent"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet2 interface [Direct Write],GetExpirationEvent method, IDWriteFontSet2.GetExpirationEvent, IDWriteFontSet2::GetExpirationEvent, GetExpirationEvent, GetExpirationEvent method [Direct Write], GetExpirationEvent method [Direct Write],IDWriteFontSet2 interface, directwrite.idwritefontset2_getexpirationevent, dwrite_3/IDWriteFontSet2::GetExpirationEvent
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
 - IDWriteFontSet2::GetExpirationEvent
 - dwrite_3/IDWriteFontSet2::GetExpirationEvent
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
 - IDWriteFontSet2::GetExpirationEvent
---

## -description

Retrieves the expiration event for the font set, if any. The expiration event is set on a system font set object if it is out of date due to fonts being installed, uninstalled, or updated. You should handle the event by getting a new system font set.



## -returns

Type: **[HANDLE](/windows/win32/winprog/windows-data-types)**

An event handle, if called on the system font set, or `nullptr` if called on a custom font set.

## -remarks

You mustn't call **CloseHandle** on the returned event handle. The handle is owned by the font set object, and it remains valid as long as you hold a reference to the font set. You can wait on the returned event, or use [RegisterWaitForSingleObject](../winbase/nf-winbase-registerwaitforsingleobject.md) to request a callback when the event is set.

## -see-also

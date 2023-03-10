---
UID: NF:wabiab.IAddrBook.Unadvise
tech.root: wab wab 
title: IAddrBook::Unadvise
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Unregisters the caller from the Windows Address Book (WAB) for notifications.
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wabiab.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wabiab.h
api_name:
 - IAddrBook::Unadvise
f1_keywords:
 - IAddrBook::Unadvise
 - wabiab/IAddrBook::Unadvise
dev_langs:
 - c++
---

## -description

Unregisters the caller from the Windows Address Book (WAB) for notifications.

## -parameters

### -param ulConnection

Value of type ULONG that specifies the connection number returned by the matching call to [IAddrBook::Advise](nf-wabiab-iaddrbook-advise.md).

## -returns

HRESULT

## -remarks

## -see-also


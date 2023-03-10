---
UID: NF:wabiab.IAddrBook.CreateOneOff
tech.root: wab wab 
title: IAddrBook::CreateOneOff
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Creates an entry identifier for a one-off address.
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
 - IAddrBook::CreateOneOff
f1_keywords:
 - IAddrBook::CreateOneOff
 - wabiab/IAddrBook::CreateOneOff
dev_langs:
 - c++
---

## -description

Creates an entry identifier for a one-off address.

## -parameters

### -param lpszName

Pointer to a string that specifies the display name of the recipient. The *lpszName* parameter can be NULL.

### -param lpszAdrType

Pointer to a string that specifies the address type of the recipient, such as FAX or SMTP. The *lpszAdrType* parameter cannot be NULL.

### -param lpszAddress

Pointer to a string that specifies the address of the recipient. The *lpszAddress* parameter cannot be NULL.

### -param ulFlags

Value of type ULONG that specifies the bitmask of flags that affect the one-off recipient. The following flags are valid in the Windows Address Book (WAB).</desc>

| Flag | Description |
|------|-------------|
| MAPI_SEND_NO_RICH_INFO | Indicates that the recipient cannot handle formatted message content. If **MAPI_SEND_NO_RICH_INFO** is set, MAPI sets the recipient's PR_SEND_RICH_INFO property to FALSE. If **MAPI_SEND_NO_RICH_INFO** is not set, MAPI sets this property to TRUE unless the recipient's messaging address (to which *lpszAddress* points) is interpreted to be an Internet address. In this case, MAPI sets PR_SEND_RICH_INFO to FALSE. |
| MAPI_UNICODE | Displays the name, address type, and address in Unicode format. If the **MAPI_UNICODE** flag is not set, these strings are displayed in ANSI format.

### -param lpcbEntryID

Pointer to a variable of type ULONG that specifies the count of bytes in the entry identifier to which the *lppEntryID* parameter points.

### -param lppEntryID

Address of a pointer to a variable of type **ENTRYID** that receives the entry identifier for the one-off recipient.

## -returns

HRESULT

## -remarks

## -see-also


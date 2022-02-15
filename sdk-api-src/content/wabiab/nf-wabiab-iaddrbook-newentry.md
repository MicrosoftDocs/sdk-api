---
UID: NF:wabiab.IAddrBook.NewEntry
tech.root: wab wab 
title: IAddrBook::NewEntry
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Displays a blank dialog box that enables the user to create a new entry.
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
 - IAddrBook::NewEntry
f1_keywords:
 - IAddrBook::NewEntry
 - wabiab/IAddrBook::NewEntry
dev_langs:
 - c++
---

## -description

Displays a blank dialog box that enables the user to create a new entry.

## -parameters

### -param ulUIParam

Value of type ULONG_PTR that specifies the parent window handle for dialog boxes.

### -param ulFlags

Reserved. Must be set to 0.

### -param cbEIDContainer

Value of type **ULONG** that specifies the size of *lpEIDContainer*.

### -param lpEIDContainer

Pointer to a variable of type **ENTRYID** that specifies the entry identifier of the container where the new address is to be created.  If the value of this parameter is NULL, the method creates the entry in the root container. Note that this differs from the MAPI implementation of **NewEntry**.

### -param cbEIDNewEntryTpl

Value of type ULONG that specifies the template entry identifier used to determine the object being created.

### -param lpEIDNewEntryTpl

Pointer to a variable of type **ENTRYID** that specifies the template entry identifier used to determine the object being created.

### -param lpcbEIDNewEntry

Pointer to a variable of type ULONG that specifies the returned size of the contents of **lppEIDNewEntry**.

### -param lppEIDNewEntry

Address of a pointer to a variable of type **ENTRYID** that receives the returned entry identifier of the new entry.

## -returns

HRESULT

## -remarks

To create a new entry in the Windows Address Book (WAB) without showing any dialog boxes, use **CreateEntry**. The *cbEIDNewEntryTpl* and the *lpEIDNewEntryTpl* are the template entry identifiers that define the kind of object being created. To obtain the template entry identifiers, open any Windows Address Book (WAB) container and request the PR_DEF_CREATE_MAILUSER or PR_DEF_CREATE_DL property from the container by calling **IMAPIProp::GetProps**. The resulting binary properties are the corresponding template identifiers.

## -see-also


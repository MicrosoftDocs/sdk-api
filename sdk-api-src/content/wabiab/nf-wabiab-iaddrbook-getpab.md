---
UID: NF:wabiab.IAddrBook.GetPAB
tech.root: wab wab 
title: IAddrBook::GetPAB
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Returns the entry identifier of the default Windows Address Book (WAB) container.
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
 - IAddrBook::GetPAB
f1_keywords:
 - IAddrBook::GetPAB
 - wabiab/IAddrBook::GetPAB
dev_langs:
 - c++
---

## -description

Returns the entry identifier of the default Windows Address Book (WAB) container.

## -parameters

### -param lpcbEntryID

Pointer to a variable of type **ULONG** that receives the returned size of the entry identifier.

### -param lppEntryID

Address of a pointer to a variable of type **ENTRYID** that receives the returned entry identifier of the default Windows Address Book (WAB) container.

## -returns

HRESULT

## -remarks

For versions of the Windows Address Book (WAB) in Internet Explorer 4 and earlier, the default Windows Address Book (WAB) container represented the entire address book; all address book contents could be accessed through this container.

For Windows Address Book (WAB) clients that specify a profile-aware Windows Address Book (WAB) session using Internet Explorer 5 and later, the default Windows Address Book (WAB) container corresponds to the current identity's 
default Contacts folder. As long as an application calls **IAddrBook::GetPAB** and manipulates data in the PAB container, 
all the data will automatically be manipulated within the current Identities 
folder.

For Windows Address Book (WAB) clients that do not request profile-aware sessions, the container returned by **IAddrBook::GetPAB** corresponds to the Contacts folder (if there is no Identity Manager) or the Shared Contacts folder (if Identities exist). This folder is available to all Windows Address Book (WAB) users. Application developers who are not interested in profiles can be assured that all their data manipulation in the PAB container is available to all users.

## -see-also


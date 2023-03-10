---
UID: NF:wabiab.IAddrBook.Details
tech.root: wab wab 
title: IAddrBook::Details
ms.date: 03/03/2021
ms.topic: language-reference
targetos: Windows
description: Displays a dialog box that shows details, and allows editing, of a particular entry in the Windows Address Book (WAB).
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
 - IAddrBook::Details
f1_keywords:
 - IAddrBook::Details
 - wabiab/IAddrBook::Details
dev_langs:
 - c++
---

## -description

Displays a dialog box that shows details, and allows editing, of a particular entry in the Windows Address Book (WAB).

## -parameters

### -param lpulUIParam

Pointer to a variable of type ULONG_PTR that receives the returned parent window handle of the returned dialog box.

### -param lpfnDismiss

DISMISSMODELESS function pointer.  This function  is called when the modeless dialog box is dismissed. Not implemented.

### -param lpvDismissContext

Not implemented.

### -param cbEntryID

Value of type ULONG that specifies the size of *lpEntryID*.

### -param lpEntryID

Pointer to a variable of type ENTRYID that specifies the entry identifier of the entry on which to display details.

### -param lpfButtonCallback

Not supported by the Windows Address Book (WAB); must be NULL.

### -param lpvButtonContext

Not supported by the Windows Address Book (WAB); must be NULL.

### -param lpszButtonText

Not supported by the Windows Address Book (WAB); must be NULL.

### -param ulFlags

Not supported by the Windows Address Book (WAB); must be NULL.

## -returns

HRESULT

## -remarks

Windows Address Book (WAB) does not support the Button callbacks. The property sheets are extensible through the **IWABExtInit** and **IShellPropSheetExt Interface** interfaces. 

## -see-also


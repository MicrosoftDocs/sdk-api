---
UID: NF:wabiab.IAddrBook.Address
tech.root: wab wab 
title: IAddrBook::Address
ms.date: 08/03/2022
ms.topic: language-reference
targetos: Windows
description: IAddrBook::Address displays the common address book dialog box.
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
 - IAddrBook::Address
f1_keywords:
 - IAddrBook::Address
 - wabiab/IAddrBook::Address
dev_langs:
 - c++
---

## -description

Displays the common address book dialog box.

## -parameters

### -param lpulUIParam

Pointer to a variable of type ULONG_PTR that specifies the handle of the parent window of the dialog box. On input, a window handle must always be passed. On output, if the DIALOG_SDI flag is set in the *lpAdrParms* parameter **ADRPARM** structure, the window handle of the modeless dialog box is returned.

### -param lpAdrParms

Pointer to a variable of type **ADRPARM** that specifies the presentation and behavior of the addressing dialog box.

### -param lppAdrList

Address of a pointer to a variable of type **ADRLIST** that specifies the current recipient list. On output, *lppAdrList* receives the address of a pointer to the **ADRLIST** where the **IAddrBook::Address** is stored. The user can set **lppAdrList** to **NULL** on input.

## -returns

HRESULT

## -remarks

The behavior of the addressing dialog box is specified by flags and parameters in *lpAdrParms*. The Windows Address Book (WAB) does not support some of the customization features of the MAPI **Address** method. The Windows Address Book (WAB) also does not support the MAPI send options dialog button.

## -see-also


---
UID: NF:iwscapi.IWSCProductList.get_Count
title: IWSCProductList::get_Count (iwscapi.h)
description: Gathers the total number of all security product providers of the specified type on the computer.
old-location: winprog\iwscproductlist_count.htm
tech.root: DevNotes
ms.assetid: A28A6D3B-DC11-418B-987F-04711358B6EE
ms.date: 12/05/2018
ms.keywords: IWSCProductList interface [Windows API],get_Count method, IWSCProductList.get_Count, IWSCProductList::get_Count, get_Count, get_Count method [Windows API], get_Count method [Windows API],IWSCProductList interface, iwscapi/IWSCProductList::get_Count, winprog.iwscproductlist_count
f1_keywords:
- iwscapi/IWSCProductList.get_Count
dev_langs:
- c++
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wscapi.lib
req.dll: Wscapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wscapi.dll
api_name:
- IWSCProductList.get_Count
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSCProductList::get_Count


## -description


Gathers the total number of all security product providers of the specified type on the computer.


## -parameters




### -param pVal [out]

A pointer to the number of providers in the list of security products on the computer.


## -returns



If the method  succeeds, returns S_OK.

If the method  fails, returns a Win32 error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iwscapi/nn-iwscapi-iwscproductlist">IWSCProductList</a>
 

 


---
UID: NF:shobjidl_core.SHGetItemFromObject
title: SHGetItemFromObject function (shobjidl_core.h)

description: Retrieves an IShellItem for an object.
old-location: shell\SHGetItemFromObject.htm
tech.root: shell
ms.assetid: 0ef494c0-81c7-4fbd-9c37-78861d8ac63b

ms.date: 12/05/2018
ms.keywords: SHGetItemFromObject, SHGetItemFromObject function [Windows Shell], _shell_SHGetItemFromObject, shell.SHGetItemFromObject, shobjidl_core/SHGetItemFromObject
ms.topic: function
f1_keywords: 
 - "shobjidl_core/SHGetItemFromObject"
dev_langs:
 - c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
api_name:
 - SHGetItemFromObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHGetItemFromObject function


## -description


Retrieves an <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> for an object.


## -parameters




### -param punk [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of the object.


### -param riid [in]

Type: <b>REFIID</b>

Reference to the desired IID.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the interface pointer requested in <i>riid</i>. This is typically <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> or a related interface.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



From the standpoint of performance, this method is preferred to <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject">SHGetIDListFromObject</a> in those cases where the IDList is already bound to a folder.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateitemfromidlist">SHCreateItemFromIDList</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shgetidlistfromobject">SHGetIDListFromObject</a>
 

 


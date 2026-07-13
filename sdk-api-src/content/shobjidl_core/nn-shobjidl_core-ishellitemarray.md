---
UID: NN:shobjidl_core.IShellItemArray
title: IShellItemArray (shobjidl_core.h)
description: Exposes methods that create and manipulate Shell item arrays.
helpviewer_keywords: ["IShellItemArray","IShellItemArray interface [Windows Shell]","IShellItemArray interface [Windows Shell]","described","_shell_IShellItemArray","shell.IShellItemArray","shobjidl_core/IShellItemArray"]
old-location: shell\IShellItemArray.htm
tech.root: shell
ms.assetid: 348213d1-c03f-4c38-9d13-3b1009d94e07
ms.date: 12/05/2018
ms.keywords: IShellItemArray, IShellItemArray interface [Windows Shell], IShellItemArray interface [Windows Shell],described, _shell_IShellItemArray, shell.IShellItemArray, shobjidl_core/IShellItemArray
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellItemArray
 - shobjidl_core/IShellItemArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IShellItemArray
---

# IShellItemArray interface


## -description

Exposes methods that create and manipulate <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">Shell item</a> arrays.

## -inheritance

The <b>IShellItemArray</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellItemArray</b> also has these types of members:

## -remarks

A shell item array may be created using one of the following functions:
                

<ul>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarray">SHCreateShellItemArray</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromdataobject">SHCreateShellItemArrayFromDataObject</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromidlists">SHCreateShellItemArrayFromIDLists</a>
</li>
<li>
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-shcreateshellitemarrayfromshellitem">SHCreateShellItemArrayFromShellItem</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumshellitems">IEnumShellItems</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>

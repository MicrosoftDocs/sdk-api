---
UID: NF:shlwapi.IUnknown_Set
title: IUnknown_Set function (shlwapi.h)
description: Changes the value of a Component Object Model (COM) interface pointer and releases the previous interface.
helpviewer_keywords: ["IUnknown_Set","IUnknown_Set function [Windows Shell]","_win32_IUnknown_Set","shell.IUnknown_Set","shlwapi/IUnknown_Set"]
old-location: shell\IUnknown_Set.htm
tech.root: shell
ms.assetid: b3c4bee2-12cb-483e-9a46-f09d63ae9a2e
ms.date: 12/05/2018
ms.keywords: IUnknown_Set, IUnknown_Set function [Windows Shell], _win32_IUnknown_Set, shell.IUnknown_Set, shlwapi/IUnknown_Set
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server, Windows Server 2003 [desktop apps only]
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
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUnknown_Set
 - shlwapi/IUnknown_Set
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-0.dll
 - ShCore.dll
 - API-MS-Win-DownLevel-shlwapi-l2-1-1.dll
 - API-MS-Win-ShCore-comhelpers-l1-1-0.dll
api_name:
 - IUnknown_Set
---

# IUnknown_Set function


## -description

Changes the value of a Component Object Model (COM) interface pointer and releases the previous interface.

## -parameters

### -param ppunk [in, out]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

The address of a COM interface pointer to receive the pointer assigned to <i>punk</i>. If the previous value of the pointer is non-<b>NULL</b>, the function releases that interface by calling its IUnkown::Release method.

### -param punk [in, optional]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The interface pointer to be copied to <i>ppunk</i>. If the value is non-<b>NULL</b>, the function increments the interface's reference count.

## -remarks

This function mimics the behavior of a smart pointer. Conceptually, the function does the following:
                
                

<ul>
<li>Releases the original interface, if <i>ppunk</i> is non-<b>NULL</b></li>
<li>Assigns <i>punk</i> to <i>ppunk</i></li>
<li>Calls IUnknown::AddRef on the interface pointed to by <i>punk</i>, if <i>punk</i> is non-<b>NULL</b>.</li>
</ul>

#### Examples


```cpp

void sample()
{
  IUnknown *punk = NULL;
  IStream* pstm = NULL;

  if (SUCCEEDED(CreateStreamOnHGlobal(NULL, TRUE, &pstm)) {
    // since punk == NULL, this merely copies the value and AddRef()s it
    IUnknown_Set(&punk, pstm);
    pstm->Release();

    if (SUCCEEDED(CreateStreamOnHGlobal(NULL, TRUE, &pstm)) {
      // this call will release the old value of punk before copying the
      // new value and AddRef()ing it
      IUnknown_Set(&punk, pstm);
      pstm->Release();
    }
  }

  // This call will release whatever punk points to, if anything.
  IUnknown_AtomcRelease((void**)&punk);

  // at this point, punk == NULL
}
```
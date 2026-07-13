---
UID: NF:shobjidl_core.IHomeGroup.IsMember
title: IHomeGroup::IsMember (shobjidl_core.h)
description: Determines whether the local computer is a member of a HomeGroup.
helpviewer_keywords: ["IHomeGroup interface [Windows Shell]","IsMember method","IHomeGroup.IsMember","IHomeGroup::IsMember","IsMember","IsMember method [Windows Shell]","IsMember method [Windows Shell]","IHomeGroup interface","_shell_IHomeGroup_IsMember","shell.IHomeGroup_IsMember","shobjidl_core/IHomeGroup::IsMember"]
old-location: shell\IHomeGroup_IsMember.htm
tech.root: shell
ms.assetid: 9ce98b11-46fd-4168-828d-a5ba8f71b7c9
ms.date: 12/05/2018
ms.keywords: IHomeGroup interface [Windows Shell],IsMember method, IHomeGroup.IsMember, IHomeGroup::IsMember, IsMember, IsMember method [Windows Shell], IsMember method [Windows Shell],IHomeGroup interface, _shell_IHomeGroup_IsMember, shell.IHomeGroup_IsMember, shobjidl_core/IHomeGroup::IsMember
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IHomeGroup::IsMember
 - shobjidl_core/IHomeGroup::IsMember
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
 - IHomeGroup.IsMember
---

# IHomeGroup::IsMember


## -description

Determines whether the local computer is a member of a HomeGroup.

## -parameters

### -param member [out]

Type: <b>BOOL*</b>

When this method returns successfully, receives <b>TRUE</b> if the local computer is a member of a HomeGroup; otherwise, <b>FALSE</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following code snippet shows how to create an instance of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup">IHomeGroup</a> and call <b>IHomeGroup::IsMember</b>.
         
                


```
#include "shobjidl.h"
#include "atlbase.h"   // For COM smart pointers
                    
CComPtr<IHomeGroup> spHomeGroup;
HRESULT hr = S_OK;
BOOL fIsHGMember = FALSE;

// Initialize the COM subsystem.
hr = CoInitialize(NULL);
if (FAILED(hr)) return hr;

// Create an instance of IHomeGroup.
hr = CoCreateInstance(CLSID_HomeGroup, 
                      NULL, 
                      CLSCTX_INPROC_SERVER, 
                      IID_PPV_ARGS(&spHomeGroup));

if (FAILED(hr)) return hr;

// fIsHGMember receives the value TRUE if the local computer is a member of a 
// HomeGroup, or FALSE if the computer is not a HomeGroup member.
hr = spHomeGroup->IsMember(&fIsHGMember);
```

## -see-also

<a href="/previous-versions/visualstudio/visual-studio-2010/ezzw7k98(v=vs.100)">CComPtr</a>



<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ihomegroup">IHomeGroup</a>
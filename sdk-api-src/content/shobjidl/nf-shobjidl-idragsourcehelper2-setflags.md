---
UID: NF:shobjidl.IDragSourceHelper2.SetFlags
title: IDragSourceHelper2::SetFlags (shobjidl.h)
description: Sets the characteristics of a drag-and-drop operation over an IDragSourceHelper object.
helpviewer_keywords: ["DSH_ALLOWDROPDESCRIPTIONTEXT","IDragSourceHelper2 interface [Windows Shell]","SetFlags method","IDragSourceHelper2.SetFlags","IDragSourceHelper2::SetFlags","SetFlags","SetFlags method [Windows Shell]","SetFlags method [Windows Shell]","IDragSourceHelper2 interface","_shell_IDragSourceHelper2_SetFlags","shell.IDragSourceHelper2_SetFlags","shobjidl/IDragSourceHelper2::SetFlags"]
old-location: shell\IDragSourceHelper2_SetFlags.htm
tech.root: shell
ms.assetid: 1fe9b753-5ac1-4b6f-9538-5259870404ec
ms.date: 12/05/2018
ms.keywords: DSH_ALLOWDROPDESCRIPTIONTEXT, IDragSourceHelper2 interface [Windows Shell],SetFlags method, IDragSourceHelper2.SetFlags, IDragSourceHelper2::SetFlags, SetFlags, SetFlags method [Windows Shell], SetFlags method [Windows Shell],IDragSourceHelper2 interface, _shell_IDragSourceHelper2_SetFlags, shell.IDragSourceHelper2_SetFlags, shobjidl/IDragSourceHelper2::SetFlags
req.header: shobjidl.h
req.include-header: 
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDragSourceHelper2::SetFlags
 - shobjidl/IDragSourceHelper2::SetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDragSourceHelper2.SetFlags
---

# IDragSourceHelper2::SetFlags


## -description

Sets the characteristics of a drag-and-drop operation over an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a> object.

## -parameters

### -param dwFlags [in]

Type: <b>DWORD</b>

The flags that determine the characteristics of a drag-and-drop operation over an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a> object.



#### DSH_ALLOWDROPDESCRIPTIONTEXT (0x0001)

Allow text specified in <a href="/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription">DROPDESCRIPTION</a> to be displayed on the drag image. If you pass this flag into the <i>dwFlags</i> parameter of <b>IDragSourceHelper2::SetFlags</b>, then the text description is rendered on top of the supplied drag image. If you pass a drag image into an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a> object, then by default, the extra text description of the drag-and-drop operation is not displayed.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
---
UID: NF:shobjidl.IDragSourceHelper2.SetFlags
title: IDragSourceHelper2::SetFlags (shobjidl.h)
author: windows-sdk-content
description: Sets the characteristics of a drag-and-drop operation over an IDragSourceHelper object.
old-location: shell\IDragSourceHelper2_SetFlags.htm
tech.root: shell
ms.assetid: 1fe9b753-5ac1-4b6f-9538-5259870404ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DSH_ALLOWDROPDESCRIPTIONTEXT, IDragSourceHelper2 interface [Windows Shell],SetFlags method, IDragSourceHelper2.SetFlags, IDragSourceHelper2::SetFlags, SetFlags, SetFlags method [Windows Shell], SetFlags method [Windows Shell],IDragSourceHelper2 interface, _shell_IDragSourceHelper2_SetFlags, shell.IDragSourceHelper2_SetFlags, shobjidl/IDragSourceHelper2::SetFlags
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDragSourceHelper2.SetFlags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDragSourceHelper2::SetFlags


## -description


Sets the characteristics of a drag-and-drop operation over an <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> object.


## -parameters




### -param dwFlags [in]

Type: <b>DWORD</b>

The flags that determine the characteristics of a drag-and-drop operation over an <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> object.



#### DSH_ALLOWDROPDESCRIPTIONTEXT (0x0001)

Allow text specified in <a href="https://msdn.microsoft.com/78757001-cac8-412d-a6c3-74bae6eb3ad8">DROPDESCRIPTION</a> to be displayed on the drag image. If you pass this flag into the <i>dwFlags</i> parameter of <b>IDragSourceHelper2::SetFlags</b>, then the text description is rendered on top of the supplied drag image. If you pass a drag image into an <a href="https://msdn.microsoft.com/d68ac8fd-4d9c-47ee-bdff-0c5bae6b5e28">IDragSourceHelper</a> object, then by default, the extra text description of the drag-and-drop operation is not displayed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




---
UID: NF:shlobj_core.IObjMgr.Remove
title: IObjMgr::Remove (shlobj_core.h)
author: windows-sdk-content
description: Removes an object from the collection of managed objects.
old-location: shell\IObjMgr_Remove.htm
tech.root: shell
ms.assetid: 21f8cce6-0d48-4b8e-8f15-1f95b112892d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IObjMgr interface [Windows Shell],Remove method, IObjMgr.Remove, IObjMgr::Remove, Remove, Remove method [Windows Shell], Remove method [Windows Shell],IObjMgr interface, _win32_IObjMgr_Remove, shell.IObjMgr_Remove, shlobj_core/IObjMgr::Remove
ms.topic: method
f1_keywords: ["shlobj_core/IObjMgr.Remove"]
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IObjMgr.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjMgr::Remove


## -description


Removes an object from the collection of managed objects.


## -parameters




### -param punk [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The address of the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the object to be removed from the list.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nn-shlobj_core-iobjmgr">IObjMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/shlobj_core/nf-shlobj_core-iobjmgr-append">IObjMgr::Append</a>
 

 


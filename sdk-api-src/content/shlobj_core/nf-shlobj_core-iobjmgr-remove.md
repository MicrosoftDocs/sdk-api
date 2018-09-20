---
UID: NF:shlobj_core.IObjMgr.Remove
title: IObjMgr::Remove
author: windows-sdk-content
description: Removes an object from the collection of managed objects.
old-location: shell\IObjMgr_Remove.htm
tech.root: shell
ms.assetid: 21f8cce6-0d48-4b8e-8f15-1f95b112892d
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: IObjMgr interface [Windows Shell],Remove method, IObjMgr.Remove, IObjMgr::Remove, Remove, Remove method [Windows Shell], Remove method [Windows Shell],IObjMgr interface, _win32_IObjMgr_Remove, shell.IObjMgr_Remove, shlobj_core/IObjMgr::Remove
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
---

# IObjMgr::Remove


## -description


Removes an object from the collection of managed objects.


## -parameters




### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

The address of the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface of the object to be removed from the list.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM error code otherwise.




## -see-also




<a href="https://msdn.microsoft.com/c0556a87-2be5-43dc-9ca6-dfbdae7e7137">IObjMgr</a>



<a href="https://msdn.microsoft.com/a616f6d1-c1dc-4c1f-acf7-915cb0f722d6">IObjMgr::Append</a>
 

 


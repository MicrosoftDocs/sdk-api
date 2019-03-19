---
UID: NF:shlobj_core.IQueryInfo.GetInfoTip
title: IQueryInfo::GetInfoTip (shlobj_core.h)
author: windows-sdk-content
description: Gets the info tip text for an item.
old-location: shell\IQueryInfo_GetInfoTip.htm
tech.root: shell
ms.assetid: 9bbaaec4-87b8-4fcc-b5df-b516ef6081ba
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetInfoTip, GetInfoTip method [Windows Shell], GetInfoTip method [Windows Shell],IQueryInfo interface, IQueryInfo interface [Windows Shell],GetInfoTip method, IQueryInfo.GetInfoTip, IQueryInfo::GetInfoTip, QITIPF_DEFAULT, QITIPF_LINKNOTARGET, QITIPF_LINKUSETARGET, QITIPF_SINGLELINE, QITIPF_USENAME, QITIPF_USESLOWTIP, _win32_IQueryInfo_GetInfoTip, shell.IQueryInfo_GetInfoTip, shlobj_core/IQueryInfo::GetInfoTip
ms.topic: method
req.header: shlobj_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IQueryInfo.GetInfoTip
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IQueryInfo::GetInfoTip


## -description


Gets the info tip text for an item.


## -parameters




### -param dwFlags

Type: <b>DWORD</b>

Flags that direct the handling of the item from which you're retrieving the info tip text. This value is commonly zero (<b>QITIPF_DEFAULT</b>). The following values are recognized.



#### QITIPF_DEFAULT (0x00000000)

No special handling.



#### QITIPF_USENAME (0x00000001)

Provide the name of the item in <i>ppwszTip</i> rather than the info tip text.



#### QITIPF_LINKNOTARGET (0x00000002)

If the item is a shortcut, retrieve the info tip text of the shortcut rather than its target.



#### QITIPF_LINKUSETARGET (0x00000004)

If the item is a shortcut, retrieve the info tip text of the shortcut's target.



#### QITIPF_USESLOWTIP (0x00000008)

Search the entire namespace for the information. This value can result in a delayed response time.



#### QITIPF_SINGLELINE (0x00000010)

<b>Windows Vista and later</b>. Put the info tip on a single line.


### -param ppwszTip [out]

Type: <b>PWSTR*</b>

The address of a Unicode string pointer that, when this method returns successfully, receives the tip string pointer. Applications that implement this method must allocate memory for <i>ppwszTip</i> by calling <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Calling applications must call <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free the memory when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the function succeeds. If no info tip text is available, <i>ppwszTip</i> is set to <b>NULL</b>. Otherwise, returns a COM-defined error value.




## -see-also




<a href="https://msdn.microsoft.com/7e256ed3-b3c7-4f9d-b3a0-e33c46fa2573">IQueryInfo</a>
 

 


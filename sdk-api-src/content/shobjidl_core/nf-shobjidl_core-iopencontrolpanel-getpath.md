---
UID: NF:shobjidl_core.IOpenControlPanel.GetPath
title: IOpenControlPanel::GetPath
author: windows-sdk-content
description: Gets the path of a specified Control Panel item.
old-location: shell\IOpenControlPanel_GetPath.htm
tech.root: shell
ms.assetid: 2043a56a-cc03-4b05-a746-de4d11ac02e7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetPath, GetPath method [Windows Shell], GetPath method [Windows Shell],IOpenControlPanel interface, IOpenControlPanel interface [Windows Shell],GetPath method, IOpenControlPanel.GetPath, IOpenControlPanel::GetPath, _shell_IOpenControlPanel_GetPath, shell.IOpenControlPanel_GetPath, shobjidl_core/IOpenControlPanel::GetPath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IOpenControlPanel.GetPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOpenControlPanel::GetPath


## -description


Gets the path of a specified Control Panel item.


## -parameters




### -param pszName [in]

Type: <b>LPCWSTR</b>

A pointer to the item's canonical name or its <b>GUID</b>. This value can be <b>NULL</b>. See Remarks for further details. For a complete list of Control Panel item canonical names, see <a href="https://msdn.microsoft.com/A02DFC9F-646D-40d8-901C-7239A820DE2C">Canonical Names of Control Panel Items</a>.


### -param pszPath [out]

Type: <b>LPWSTR</b>

When this method returns, contains the path of the specified Control Panel item as a Unicode string.


### -param cchPath [in]

Type: <b>UINT</b>

The size of the buffer pointed to by <i>pszPath</i>, in WCHARs.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <i>pszName</i> points to the item's canonical name or <b>GUID</b>, then the path returned is in one of these two forms, depending on the most recent Control Panel view (Classic View or Category View):

                


```cpp
::{CLSID_ControlPanel}\::{item guid}
::{CLSID_ControlPanelCategory}\categoryId\::{item guid}

```


If <i>pszName</i> is <b>NULL</b> then one of these two values is returned:

                


```cpp
::{CLSID_ControlPanel}
::{CLSID_ControlPanelCategory}

```





## -see-also




<a href="https://msdn.microsoft.com/library/Bb757044(v=MSDN.10).aspx">Developing for the Control Panel</a>



<a href="https://msdn.microsoft.com/fbf86553-7aa1-4a0f-9775-5f71f41b1705">IOpenControlPanel</a>
 

 


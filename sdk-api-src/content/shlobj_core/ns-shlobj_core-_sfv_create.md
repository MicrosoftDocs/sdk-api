---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SFV_CREATE structure


## -description


This structure is used with the <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a> function.


## -struct-fields




### -field cbSize

Type: <b>UINT</b>

The size of the <b>SFV_CREATE</b> structure, in bytes.


### -field pshf

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

The <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface of the folder for which to create the view.


### -field psvOuter

Type: <b><a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a>*</b>

A pointer to the parent <a href="https://msdn.microsoft.com/91438583-e4f1-456f-a130-2a45846fd725">IShellView</a> interface. This parameter may be <b>NULL</b>. This parameter is used only when the view created by <a href="https://msdn.microsoft.com/f2948a6d-84a5-456b-b328-ba76dba46e9d">SHCreateShellFolderView</a> is hosted in a common dialog box.


### -field psfvcb

Type: <b><a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/0cd2bce8-d77a-4140-869b-707aaa279796">IShellFolderViewCB</a> interface that handles the view's callbacks when various events occur. This parameter may be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/bf89ac6e-6c2e-4944-885c-9ab62f58fe71">ICommDlgBrowser</a>
 

 


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

# ICommDlgBrowser2::GetViewFlags


## -description


Called when the view must determine if special customization needs to be made for the common dialog browser.


## -parameters




### -param pdwFlags

Type: <b>DWORD*</b>

A pointer to a <b>DWORD</b> value that controls the behavior of the view when in common dialog mode.



#### CDB2GVF_SHOWALLFILES (0x00000001)

0x00000001. All files, including hidden and system files, should be shown. In Windows XP, this is the only recognized flag.



#### CDB2GVF_ISFILESAVE (0x00000002)

0x00000002. This browser is designated to choose a file to save.



#### CDB2GVF_ALLOWPREVIEWPANE (0x00000004)

0x00000004. Not used.



#### CDB2GVF_NOSELECTVERB (0x00000008)

0x00000008. Do not show a "<code>select</code>" verb on an item's context menu.



#### CDB2GVF_NOINCLUDEITEM (0x00000010)

0x00000010. <a href="https://msdn.microsoft.com/f483dda2-5384-42b5-97ca-c7c6793d19a7">IncludeObject</a> should not be called.



#### CDB2GVF_ISFOLDERPICKER (0x00000020)

0x00000020. This browser is designated to pick folders.



#### CDB2GVF_ADDSHIELD (0x00000040)

0x00000040. <b>Windows 7 and later</b>. Displays a UAC shield on the selected item when CDB2GVF_NOSELECTVERB is not specified.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07a416a2-340d-4308-a6f3-cf6f19f3c906">ICommDlgBrowser2</a>
 

 


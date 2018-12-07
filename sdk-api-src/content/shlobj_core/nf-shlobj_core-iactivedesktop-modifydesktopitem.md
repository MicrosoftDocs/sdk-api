---
UID: NF:shlobj_core.IActiveDesktop.ModifyDesktopItem
title: IActiveDesktop::ModifyDesktopItem
author: windows-sdk-content
description: Modifies the desktop item.
old-location: lwef\iactivedesktop_modifydesktopitem.htm
tech.root: lwef
ms.assetid: f80a0b49-3fa9-4041-833e-1e809a606a0c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: COMP_ELEM_ALL, COMP_ELEM_CHECKED, COMP_ELEM_CURITEMSTATE, COMP_ELEM_FRIENDLYNAME, COMP_ELEM_NOSCROLL, COMP_ELEM_ORIGINAL_CSI, COMP_ELEM_POS_LEFT, COMP_ELEM_POS_TOP, COMP_ELEM_POS_ZINDEX, COMP_ELEM_RESTORED_CSI, COMP_ELEM_SIZE_HEIGHT, COMP_ELEM_SIZE_WIDTH, COMP_ELEM_SOURCE, COMP_ELEM_TYPE, IActiveDesktop interface [Legacy Windows Environment Features],ModifyDesktopItem method, IActiveDesktop.ModifyDesktopItem, IActiveDesktop::ModifyDesktopItem, ModifyDesktopItem, ModifyDesktopItem method [Legacy Windows Environment Features], ModifyDesktopItem method [Legacy Windows Environment Features],IActiveDesktop interface, _win32_IActiveDesktop_ModifyDesktopItem, lwef.iactivedesktop_modifydesktopitem, shell.iactivedesktop_modifydesktopitem, shlobj/IActiveDesktop::ModifyDesktopItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.dll: Shlobj_core.h (version 4.71 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shlobj_core.h
api_name:
 - IActiveDesktop.ModifyDesktopItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IActiveDesktop::ModifyDesktopItem


## -description


Modifies the desktop item.


## -parameters




### -param pcomp [in, out]

Type: <b>LPCCOMPONENT</b>

The address of the <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a> structure that contains the modifications. The desktop item associated with the <b>wszSource</b> member of the structure will be modified. 


### -param dwFlags

Type: <b>DWORD</b>

An unsigned long integer value containing the flags used for the modification. This can be one of the following values. 



#### COMP_ELEM_ALL



#### COMP_ELEM_CHECKED



#### COMP_ELEM_CURITEMSTATE



#### COMP_ELEM_FRIENDLYNAME



#### COMP_ELEM_NOSCROLL



#### COMP_ELEM_ORIGINAL_CSI



#### COMP_ELEM_POS_LEFT



#### COMP_ELEM_POS_TOP



#### COMP_ELEM_POS_ZINDEX



#### COMP_ELEM_RESTORED_CSI



#### COMP_ELEM_SIZE_HEIGHT



#### COMP_ELEM_SIZE_WIDTH



#### COMP_ELEM_SOURCE



#### COMP_ELEM_TYPE


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The client application must call <a href="https://msdn.microsoft.com/3bac5af5-f4a6-4822-83de-11633beef88a">IActiveDesktop::ApplyChanges</a> separately to update the registry. For example, to change the friendly name, first call this function with either <b>COMP_ELEM_FRIENDLYNAME</b> or <b>COMP_ELEM_ALL</b> in the <b>dwFlags</b> member of <a href="https://msdn.microsoft.com/2692a2d6-1d33-410f-987c-8388c636cae6">COMPONENT</a>. Then call <b>IActiveDesktop::ApplyChanges</b>.




## -see-also




<a href="https://msdn.microsoft.com/4d572b86-36e8-417b-857c-eb477c04c691">IActiveDesktop</a>
 

 


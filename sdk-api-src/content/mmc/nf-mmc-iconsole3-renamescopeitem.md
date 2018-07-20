---
UID: NF:mmc.IConsole3.RenameScopeItem
title: IConsole3::RenameScopeItem
author: windows-sdk-content
description: The RenameScopeItem method programmatically puts the specified scope item in rename mode. Subsequently, the user can manually enter the new name.
old-location: mmc\iconsole3_renamescopeitem.htm
old-project: mmc
ms.assetid: ebbdc395-e94f-4e86-965c-59bf7a49bbeb
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: IConsole3 interface [MMC],RenameScopeItem method, IConsole3.RenameScopeItem, IConsole3::RenameScopeItem, RenameScopeItem, RenameScopeItem method [MMC], RenameScopeItem method [MMC],IConsole3 interface, _slate_iconsole3_renamescopeitem, mmc.iconsole3_renamescopeitem, mmc/IConsole3::RenameScopeItem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole3.RenameScopeItem
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IConsole3::RenameScopeItem


## -description


The 
<b>RenameScopeItem</b> method programmatically puts the specified scope item in rename mode. Subsequently, the user can manually enter the new name.

Use this method only when an item is created and immediately must be put in rename mode. Use of this method for other scenarios, such as being called after an item has been selected, is not supported and may have unexpected results.


## -parameters




### -param hScopeItem [in]

The scope item put in rename mode.


## -returns



If successful, the return value is <b>S_OK</b>. If unsuccessful, the method returns <b>E_FAIL</b>.




## -remarks



For this method to succeed, the item put in rename mode must have the Rename verb enabled, and the scope pane must be not be invisible.




## -see-also




<a href="https://msdn.microsoft.com/be3d42a4-a18a-40a5-99fc-2cf2a848c564">IConsole3</a>



<a href="https://msdn.microsoft.com/a667f638-88bb-4758-8df7-478b0d6c18c4">IResultData2::RenameResultItem</a>
 

 


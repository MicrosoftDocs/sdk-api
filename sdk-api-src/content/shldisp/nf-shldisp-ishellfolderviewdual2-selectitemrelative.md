---
UID: NF:shldisp.IShellFolderViewDual2.SelectItemRelative
title: IShellFolderViewDual2::SelectItemRelative
author: windows-driver-content
description: Selects an item relative to the current item.
old-location: shell\IShellFolderViewDual2_SelectItemRelative.htm
old-project: shell
ms.assetid: 421a039e-49d6-4a93-958a-48c7e847fa6b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IShellFolderViewDual2 interface [Windows Shell],SelectItemRelative method, IShellFolderViewDual2.SelectItemRelative, IShellFolderViewDual2::SelectItemRelative, SelectItemRelative, SelectItemRelative method [Windows Shell], SelectItemRelative method [Windows Shell],IShellFolderViewDual2 interface, _shell_IShellFolderViewDual2_SelectItemRelative, shell.IShellFolderViewDual2_SelectItemRelative, shldisp/IShellFolderViewDual2::SelectItemRelative
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shldisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shldisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AUTOCOMPLETEOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shldisp.h
api_name:
-	IShellFolderViewDual2.SelectItemRelative
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5.0
---

# IShellFolderViewDual2::SelectItemRelative


## -description


Selects an item relative to the current item.


## -parameters




### -param iRelative [in]

Type: <b>int</b>

The offset of the item to be selected in relation to the current item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The current item is defined as the item in the view with the SVSI_SELECTIONMARK state. If there is no item with SVSI_SELECTIONMARK, the method returns S_FALSE and does nothing.




---
UID: NF:mmc.IHeaderCtrl.SetColumnText
title: IHeaderCtrl::SetColumnText
author: windows-sdk-content
description: Sets the text of the title in a specific column.
old-location: mmc\iheaderctrl_setcolumntext.htm
old-project: MMC
ms.assetid: B760D7E1-DE2D-4E1A-898C-5EC1E99E9B91
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IHeaderCtrl interface [MMC],SetColumnText method, IHeaderCtrl.SetColumnText, IHeaderCtrl::SetColumnText, SetColumnText, SetColumnText method [MMC], SetColumnText method [MMC],IHeaderCtrl interface, mmc.iheaderctrl_setcolumntext, mmc/IHeaderCtrl::SetColumnText
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
req.idl: Mmc.idl
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
 - IHeaderCtrl.SetColumnText
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IHeaderCtrl::SetColumnText


## -description


Sets the text of the title in a specific column.


## -parameters




### -param nCol [in]

A zero-based index that specifies the location of the column.


### -param title [in]

A pointer to the string that represents the title of the column being inserted. This string can have  a maximum length of MAX_PATH characters.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/64da2c79-2ede-4b17-a706-8e5cc0ade007">IHeaderCtrl</a>
 

 


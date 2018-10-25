---
UID: NF:mmc.IHeaderCtrl.GetColumnText
title: IHeaderCtrl::GetColumnText
author: windows-sdk-content
description: Retrieves text from a specified column.
old-location: mmc\iheaderctrl_getcolumntext.htm
tech.root: mmc
ms.assetid: 854FC5F0-8049-4A98-948F-F1BF78788B88
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: GetColumnText, GetColumnText method [MMC], GetColumnText method [MMC],IHeaderCtrl interface, IHeaderCtrl interface [MMC],GetColumnText method, IHeaderCtrl.GetColumnText, IHeaderCtrl::GetColumnText, mmc.iheaderctrl_getcolumntext, mmc/IHeaderCtrl::GetColumnText
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IHeaderCtrl.GetColumnText
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHeaderCtrl::GetColumnText


## -description


Retrieves text from a specified column.


## -parameters




### -param nCol [in]

A zero-based index that identifies the column from which the text is to be retrieved.


### -param pText [out]

A pointer to the address of the text to be retrieved. This pointer must not be <b>NULL</b>. The user must call 
<b>CoTaskMemFree</b> on the returned text.


## -returns



This method can return one of these values.




## -remarks



<b>GetColumnText</b> allocates the string for the result and stores its pointer at the location specified by pText. The caller must free the memory using 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a>.




## -see-also




<a href="https://msdn.microsoft.com/64da2c79-2ede-4b17-a706-8e5cc0ade007">IHeaderCtrl</a>
 

 


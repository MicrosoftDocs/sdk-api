---
UID: NF:mmc.IExtendTaskPad.GetListPadInfo
title: IExtendTaskPad::GetListPadInfo
author: windows-sdk-content
description: The IExtendTaskPad::GetListPadInfo method is used for list-view taskpads only.
old-location: mmc\iextendtaskpad_getlistpadinfo.htm
old-project: MMC
ms.assetid: 73e9d281-9bf9-4a50-b3e8-226ed3593f7a
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetListPadInfo, GetListPadInfo method [MMC], GetListPadInfo method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],GetListPadInfo method, IExtendTaskPad.GetListPadInfo, IExtendTaskPad::GetListPadInfo, _slate_iextendtaskpad_getlistpadinfo, mmc.iextendtaskpad_getlistpadinfo, mmc/IExtendTaskPad::GetListPadInfo
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
 - Mmc.h
api_name:
 - IExtendTaskPad.GetListPadInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IExtendTaskPad::GetListPadInfo


## -description


The <b>IExtendTaskPad::GetListPadInfo</b> method is used for list-view taskpads only. It enables MMC to get the title text for the list control, the text for an optional button, and the command ID passed to 
<a href="https://msdn.microsoft.com/c20d87f9-a5a0-41b9-b343-a11e8b41ed71">IExtendTaskPad::TaskNotify</a> when that optional button is clicked.


## -parameters




### -param pszGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the ppViewType parameter when MMC calls <a href="https://msdn.microsoft.com/d2575f79-d646-41b5-84a5-768402cfb826">IComponent::GetResultViewType</a> to display the taskpad. If no group name is specified, szGroup is a <b>NULL</b> string.


### -param lpListPadInfo [out]

A pointer to an 
<a href="https://msdn.microsoft.com/53e3cd8f-9d78-4edc-a0bb-3b409857561f">MMC_LISTPAD_INFO</a> structure that the snap-in must fill in with the title text for the list control, the text for an optional button, and the command ID passed to <a href="https://msdn.microsoft.com/c20d87f9-a5a0-41b9-b343-a11e8b41ed71">IExtendTaskPad::TaskNotify</a> when that optional button is clicked.

Be aware that the caller (MMC) allocates the memory for the 
<a href="https://msdn.microsoft.com/53e3cd8f-9d78-4edc-a0bb-3b409857561f">MMC_LISTPAD_INFO</a> structure.


## -returns



This method can return one of these values.




## -remarks



If the snap-in is not a list-view taskpad, this method is not called by MMC.




## -see-also




<a href="https://msdn.microsoft.com/30f5b526-d2d5-48a6-be5f-d0f2ba9397c4">IExtendTaskPad</a>
 

 


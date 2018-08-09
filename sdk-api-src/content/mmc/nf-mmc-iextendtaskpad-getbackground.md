---
UID: NF:mmc.IExtendTaskPad.GetBackground
title: IExtendTaskPad::GetBackground
author: windows-sdk-content
description: The IExtendTaskPad::GetBackground method enables MMC to get the taskpad's background image to display in taskpads that use MMC taskpad templates.
old-location: mmc\iextendtaskpad_getbackground.htm
old-project: MMC
ms.assetid: e34fc088-61d7-46a8-b493-8255a733d521
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetBackground, GetBackground method [MMC], GetBackground method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],GetBackground method, IExtendTaskPad.GetBackground, IExtendTaskPad::GetBackground, _slate_iextendtaskpad_getbackground, mmc.iextendtaskpad_getbackground, mmc/IExtendTaskPad::GetBackground
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
 - IExtendTaskPad.GetBackground
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IExtendTaskPad::GetBackground


## -description


The <b>IExtendTaskPad::GetBackground</b> method enables MMC to get the taskpad's background image to display in taskpads that use MMC taskpad templates.


## -parameters




### -param pszGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the ppViewType parameter when MMC calls IComponent::GetResultViewType to display the taskpad. If no group name is specified, pszGroup is a <b>NULL</b> string.


### -param pTDO [out]

A pointer to an 
<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a> structure that the snap-in must fill in to specify the image to be displayed as the background for the taskpad specified by pszGroup.

Be aware that the caller (MMC) allocates the memory for the 
MMC_TASK_DISPLAY_OBJECT structure.


## -returns



This method can return one of these values.




## -remarks



Allocate the strings in the 
<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a> or 
<a href="https://msdn.microsoft.com/a46f1b86-883e-4eca-a3f8-d18c6a4d64e5">MMC_TASK_DISPLAY_SYMBOL</a> structure specified in the pTDO parameter with the COM API function CoTaskMemAlloc (or the equivalent) and MMC will release it.




## -see-also




<a href="https://msdn.microsoft.com/30f5b526-d2d5-48a6-be5f-d0f2ba9397c4">IExtendTaskPad</a>



<a href="https://msdn.microsoft.com/9895eef1-7870-4092-8bf9-c13f38b74173">MMC_TASK_DISPLAY_BITMAP</a>



<a href="https://msdn.microsoft.com/ff43f0ea-2f33-4ed9-b5a5-484db2ffe3ad">MMC_TASK_DISPLAY_OBJECT</a>



<a href="https://msdn.microsoft.com/a46f1b86-883e-4eca-a3f8-d18c6a4d64e5">MMC_TASK_DISPLAY_SYMBOL</a>
 

 


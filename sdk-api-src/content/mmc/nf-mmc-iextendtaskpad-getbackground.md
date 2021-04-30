---
UID: NF:mmc.IExtendTaskPad.GetBackground
title: IExtendTaskPad::GetBackground (mmc.h)
description: The IExtendTaskPad::GetBackground method enables MMC to get the taskpad's background image to display in taskpads that use MMC taskpad templates.
helpviewer_keywords: ["GetBackground","GetBackground method [MMC]","GetBackground method [MMC]","IExtendTaskPad interface","IExtendTaskPad interface [MMC]","GetBackground method","IExtendTaskPad.GetBackground","IExtendTaskPad::GetBackground","_slate_iextendtaskpad_getbackground","mmc.iextendtaskpad_getbackground","mmc/IExtendTaskPad::GetBackground"]
old-location: mmc\iextendtaskpad_getbackground.htm
tech.root: mmc
ms.assetid: e34fc088-61d7-46a8-b493-8255a733d521
ms.date: 12/05/2018
ms.keywords: GetBackground, GetBackground method [MMC], GetBackground method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],GetBackground method, IExtendTaskPad.GetBackground, IExtendTaskPad::GetBackground, _slate_iextendtaskpad_getbackground, mmc.iextendtaskpad_getbackground, mmc/IExtendTaskPad::GetBackground
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExtendTaskPad::GetBackground
 - mmc/IExtendTaskPad::GetBackground
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IExtendTaskPad.GetBackground
---

# IExtendTaskPad::GetBackground


## -description

The <b>IExtendTaskPad::GetBackground</b> method enables MMC to get the taskpad's background image to display in taskpads that use MMC taskpad templates.

## -parameters

### -param pszGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the ppViewType parameter when MMC calls IComponent::GetResultViewType to display the taskpad. If no group name is specified, pszGroup is a <b>NULL</b> string.

### -param pTDO [out]

A pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a> structure that the snap-in must fill in to specify the image to be displayed as the background for the taskpad specified by pszGroup.

Be aware that the caller (MMC) allocates the memory for the 
MMC_TASK_DISPLAY_OBJECT structure.

## -returns

This method can return one of these values.

## -remarks

Allocate the strings in the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a> or 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a> structure specified in the pTDO parameter with the COM API function CoTaskMemAlloc (or the equivalent) and MMC will release it.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iextendtaskpad">IExtendTaskPad</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_bitmap">MMC_TASK_DISPLAY_BITMAP</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_object">MMC_TASK_DISPLAY_OBJECT</a>



<a href="/windows/desktop/api/mmc/ns-mmc-mmc_task_display_symbol">MMC_TASK_DISPLAY_SYMBOL</a>
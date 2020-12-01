---
UID: NF:mmc.IExtendTaskPad.GetListPadInfo
title: IExtendTaskPad::GetListPadInfo (mmc.h)
description: The IExtendTaskPad::GetListPadInfo method is used for list-view taskpads only.
helpviewer_keywords: ["GetListPadInfo","GetListPadInfo method [MMC]","GetListPadInfo method [MMC]","IExtendTaskPad interface","IExtendTaskPad interface [MMC]","GetListPadInfo method","IExtendTaskPad.GetListPadInfo","IExtendTaskPad::GetListPadInfo","_slate_iextendtaskpad_getlistpadinfo","mmc.iextendtaskpad_getlistpadinfo","mmc/IExtendTaskPad::GetListPadInfo"]
old-location: mmc\iextendtaskpad_getlistpadinfo.htm
tech.root: mmc
ms.assetid: 73e9d281-9bf9-4a50-b3e8-226ed3593f7a
ms.date: 12/05/2018
ms.keywords: GetListPadInfo, GetListPadInfo method [MMC], GetListPadInfo method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],GetListPadInfo method, IExtendTaskPad.GetListPadInfo, IExtendTaskPad::GetListPadInfo, _slate_iextendtaskpad_getlistpadinfo, mmc.iextendtaskpad_getlistpadinfo, mmc/IExtendTaskPad::GetListPadInfo
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
 - IExtendTaskPad::GetListPadInfo
 - mmc/IExtendTaskPad::GetListPadInfo
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
 - IExtendTaskPad.GetListPadInfo
---

# IExtendTaskPad::GetListPadInfo


## -description

The <b>IExtendTaskPad::GetListPadInfo</b> method is used for list-view taskpads only. It enables MMC to get the title text for the list control, the text for an optional button, and the command ID passed to 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> when that optional button is clicked.

## -parameters

### -param pszGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the ppViewType parameter when MMC calls <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> to display the taskpad. If no group name is specified, szGroup is a <b>NULL</b> string.

### -param lpListPadInfo [out]

A pointer to an 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_listpad_info">MMC_LISTPAD_INFO</a> structure that the snap-in must fill in with the title text for the list control, the text for an optional button, and the command ID passed to <a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> when that optional button is clicked.

Be aware that the caller (MMC) allocates the memory for the 
<a href="/windows/desktop/api/mmc/ns-mmc-mmc_listpad_info">MMC_LISTPAD_INFO</a> structure.

## -returns

This method can return one of these values.

## -remarks

If the snap-in is not a list-view taskpad, this method is not called by MMC.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iextendtaskpad">IExtendTaskPad</a>
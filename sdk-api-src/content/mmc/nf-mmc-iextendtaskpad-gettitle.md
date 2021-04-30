---
UID: NF:mmc.IExtendTaskPad.GetTitle
title: IExtendTaskPad::GetTitle (mmc.h)
description: The IExtendTaskPad::GetTitle method enables MMC to get the taskpad title text to display in taskpads that use MMC taskpad templates.
helpviewer_keywords: ["GetTitle","GetTitle method [MMC]","GetTitle method [MMC]","IExtendTaskPad interface","IExtendTaskPad interface [MMC]","GetTitle method","IExtendTaskPad.GetTitle","IExtendTaskPad::GetTitle","_slate_iextendtaskpad_gettitle","mmc.iextendtaskpad_gettitle","mmc/IExtendTaskPad::GetTitle"]
old-location: mmc\iextendtaskpad_gettitle.htm
tech.root: mmc
ms.assetid: d04eb4fe-bcb2-457f-8d22-434352068056
ms.date: 12/05/2018
ms.keywords: GetTitle, GetTitle method [MMC], GetTitle method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],GetTitle method, IExtendTaskPad.GetTitle, IExtendTaskPad::GetTitle, _slate_iextendtaskpad_gettitle, mmc.iextendtaskpad_gettitle, mmc/IExtendTaskPad::GetTitle
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
 - IExtendTaskPad::GetTitle
 - mmc/IExtendTaskPad::GetTitle
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
 - IExtendTaskPad.GetTitle
---

# IExtendTaskPad::GetTitle


## -description

The <b>IExtendTaskPad::GetTitle</b> method enables MMC to get the taskpad title text to display in taskpads that use MMC taskpad templates.

## -parameters

### -param pszGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the <i>ppViewType</i> parameter when MMC calls <a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> to display the taskpad. If no group name is specified, <i>pszGroup</i> is a <b>NULL</b> string.

### -param pszTitle [out]

A pointer to the address of a null-terminated string that contains the title for the taskpad specified by <i>pszGroup</i>. This text is displayed at the top of the taskpad as the title for the entire taskpad. If <i>pszTitle</i> points to a <b>NULL</b> string, no title is displayed.

## -returns

This method can return one of these values.

## -remarks

Allocate the <i>pszTitle</i> string with the COM API function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release it.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iextendtaskpad">IExtendTaskPad</a>
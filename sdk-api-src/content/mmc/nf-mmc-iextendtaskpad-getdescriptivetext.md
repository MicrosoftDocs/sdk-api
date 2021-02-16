---
UID: NF:mmc.IExtendTaskPad.GetDescriptiveText
title: IExtendTaskPad::GetDescriptiveText (mmc.h)
description: The IExtendTaskPad::GetDescriptiveText method enables MMC to get the taskpad's descriptive text to display in taskpads that use MMC taskpad templates.
helpviewer_keywords: ["GetDescriptiveText","GetDescriptiveText method [MMC]","GetDescriptiveText method [MMC]","IExtendTaskPad interface","IExtendTaskPad interface [MMC]","GetDescriptiveText method","IExtendTaskPad.GetDescriptiveText","IExtendTaskPad::GetDescriptiveText","_slate_iextendtaskpad_getdescriptivetext","mmc.iextendtaskpad_getdescriptivetext","mmc/IExtendTaskPad::GetDescriptiveText"]
old-location: mmc\iextendtaskpad_getdescriptivetext.htm
tech.root: mmc
ms.assetid: e8d02b4e-703f-42fe-a55c-cc5cf84e8f74
ms.date: 12/05/2018
ms.keywords: GetDescriptiveText, GetDescriptiveText method [MMC], GetDescriptiveText method [MMC],IExtendTaskPad interface, IExtendTaskPad interface [MMC],GetDescriptiveText method, IExtendTaskPad.GetDescriptiveText, IExtendTaskPad::GetDescriptiveText, _slate_iextendtaskpad_getdescriptivetext, mmc.iextendtaskpad_getdescriptivetext, mmc/IExtendTaskPad::GetDescriptiveText
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
 - IExtendTaskPad::GetDescriptiveText
 - mmc/IExtendTaskPad::GetDescriptiveText
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
 - IExtendTaskPad.GetDescriptiveText
---

# IExtendTaskPad::GetDescriptiveText


## -description

The <b>IExtendTaskPad::GetDescriptiveText</b> method enables MMC to get the taskpad's descriptive text to display in taskpads that use MMC taskpad templates.

## -parameters

### -param pszGroup [in]

A pointer to a null-terminated string that contains the group name that identifies the taskpad. The group name is the string that follows the hash (#) in the string passed in the ppViewType parameter when MMC calls 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-getresultviewtype">IComponent::GetResultViewType</a> to display the taskpad. If no group name is specified, szGroup is a <b>NULL</b> string.

### -param pszDescriptiveText [out]

A pointer to the address of a null-terminated string that contains the descriptive text for the taskpad specified by pszGroup. This text is displayed at the top of the taskpad beneath the title for the entire taskpad. This text can be a phrase that serves as a subtitle or instructions (such as "Click an action to perform.").

If pszDescriptiveText points to a <b>NULL</b> string, no descriptive text is displayed.

## -returns

This method can return one of these values.

## -remarks

Allocate the pszDescriptiveText string with the COM API function 
<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release it.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iextendtaskpad">IExtendTaskPad</a>
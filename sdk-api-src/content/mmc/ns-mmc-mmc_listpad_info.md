---
UID: NS:mmc._MMC_LISTPAD_INFO
title: MMC_LISTPAD_INFO (mmc.h)
description: The MMC_LISTPAD_INFO structure is introduced in MMC 1.1.
helpviewer_keywords: ["MMC_LISTPAD_INFO","MMC_LISTPAD_INFO structure [MMC]","_slate_mmc_listpad_info","mmc.mmc_listpad_info","mmc/MMC_LISTPAD_INFO"]
old-location: mmc\mmc_listpad_info.htm
tech.root: mmc
ms.assetid: 53e3cd8f-9d78-4edc-a0bb-3b409857561f
ms.date: 12/05/2018
ms.keywords: MMC_LISTPAD_INFO, MMC_LISTPAD_INFO structure [MMC], _slate_mmc_listpad_info, mmc.mmc_listpad_info, mmc/MMC_LISTPAD_INFO
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
req.typenames: MMC_LISTPAD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MMC_LISTPAD_INFO
 - mmc/_MMC_LISTPAD_INFO
 - MMC_LISTPAD_INFO
 - mmc/MMC_LISTPAD_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - MMC_LISTPAD_INFO
---

# MMC_LISTPAD_INFO structure


## -description

The 
<b>MMC_LISTPAD_INFO</b> structure is introduced in MMC 1.1.

The 
<b>MMC_LISTPAD_INFO</b> structure is filled in by the 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getlistpadinfo">IExtendTaskPad::GetListPadInfo</a> method to specify the following information for a list view taskpad:
<ul>
<li>Title text for the list control</li>
<li>Text for an optional button</li>
<li>The command ID passed to 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> when that button is clicked.</li>
</ul>

## -struct-fields

### -field szTitle

A pointer to a null-terminated string that contains the text placed directly above the list control. This text can be the label for the objects within the list control (such as "Printers" if the list contains printers) or instructions (such as "Select a printer and click an action to perform.").

If <b>szTitle</b> is <b>NULL</b> or empty, no title is displayed for the list control.

Be aware that the <b>szTitle</b> member is not the same as the <i>pszTitle</i> parameter for 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-gettitle">IExtendTaskPad::GetTitle</a>. The <b>IExtendTaskPad::GetTitle</b> method returns the title for the entire taskpad that appears at the top of the taskpad and appears on every standard MMC taskpad. The <b>szTitle</b> member of 
<b>MMC_LISTPAD_INFO</b> is the label for the list control and appears only on MMC list view taskpads.

### -field szButtonText

A pointer to a null-terminated string that contains the text placed on a button that is directly above the list control and to the right of the <b>szTitle</b> text.

When the user clicks this button on the taskpad, MMC calls the 
<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> method of the snap-in and passes the value specified in <b>nCommandID</b> as a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure in the arg parameter. The <b>VARIANT</b> passed to 
<b>TaskNotify</b> has a <b>vt</b> member set to <b>VT_I4</b> and an <b>lVal</b> member that contains the command ID.

To make the button to appear with no text, set <b>szButtonText</b> to an empty string.

To hide this button to appear on the taskpad, set <b>szButtonText</b> to <b>NULL</b>.

### -field nCommandID

Value that serves as an identifier for the button specified by <b>szButtonText</b>. It is recommended that you make this value unique to each taskpad to help identify the taskpad that sent the button-click notification.

When the user clicks this button, MMC calls the <a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a> method of the snap-in and passes this value as a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> in the arg parameter.

This value is ignored if <b>szButtonText</b> is <b>NULL</b>.

## -remarks

Allocate the <b>szTitle</b> and <b>szButtonText</b> strings with the COM API function <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> (or the equivalent) and MMC will release it.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-getlistpadinfo">IExtendTaskPad::GetListPadInfo</a>



<a href="/windows/desktop/api/mmc/nf-mmc-iextendtaskpad-tasknotify">IExtendTaskPad::TaskNotify</a>
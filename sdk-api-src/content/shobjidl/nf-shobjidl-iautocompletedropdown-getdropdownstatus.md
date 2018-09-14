---
UID: NF:shobjidl.IAutoCompleteDropDown.GetDropDownStatus
title: IAutoCompleteDropDown::GetDropDownStatus
author: windows-sdk-content
description: Gets the current display status of the autocomplete drop-down list.
old-location: shell\IAutoCompleteDropDown_GetDropDownStatus.htm
tech.root: shell
ms.assetid: 824c435c-e8ee-4435-a779-bae3ef721613
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ACDD_VISIBLE, GetDropDownStatus, GetDropDownStatus method [Windows Shell], GetDropDownStatus method [Windows Shell],IAutoCompleteDropDown interface, IAutoCompleteDropDown interface [Windows Shell],GetDropDownStatus method, IAutoCompleteDropDown.GetDropDownStatus, IAutoCompleteDropDown::GetDropDownStatus, _shell_IAutoCompleteDropDown_GetDropDownStatus, shell.IAutoCompleteDropDown_GetDropDownStatus, shobjidl/IAutoCompleteDropDown::GetDropDownStatus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Browseui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Browseui.dll
api_name:
 - IAutoCompleteDropDown.GetDropDownStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAutoCompleteDropDown::GetDropDownStatus


## -description


Gets the current display status of the autocomplete drop-down list.


## -parameters




### -param pdwFlags [out]

Type: <b>DWORD*</b>

A pointer to a value indicating whether the autocomplete drop-down list is currently displayed. This parameter can be <b>NULL</b> on entry if this information is not needed. The following values are recognized as the target of this pointer.



#### (0x0000)

The list is not visible.



#### ACDD_VISIBLE (0x0001)

The list is visible.


### -param ppwszString [out]

Type: <b>LPWSTR*</b>

A pointer to a buffer containing the first select item in the drop-down list, if the value pointed to by <i>pdwFlags</i> is <b>ACDD_VISIBLE</b>. This value can be <b>NULL</b> on entry if this information is not needed.
            
                    

If <i>pdwFlags</i> is zero on exit, then this value will be <b>NULL</b>.

If this value is not <b>NULL</b> on exit, the buffer it points to must be freed using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> when it is no longer needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/1f956d61-6a09-464e-bfe8-0b3bcb9ea181">IAutoCompleteDropDown</a>
 

 


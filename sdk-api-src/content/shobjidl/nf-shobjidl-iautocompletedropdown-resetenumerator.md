---
UID: NF:shobjidl.IAutoCompleteDropDown.ResetEnumerator
title: IAutoCompleteDropDown::ResetEnumerator
author: windows-sdk-content
description: Forces the autocomplete object to refresh its list of suggestions when the list is visible.
old-location: shell\IAutoCompleteDropDown_ResetEnumerator.htm
old-project: shell
ms.assetid: 9a880b2a-190a-45ea-8672-f2d0247987ed
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAutoCompleteDropDown interface [Windows Shell],ResetEnumerator method, IAutoCompleteDropDown.ResetEnumerator, IAutoCompleteDropDown::ResetEnumerator, ResetEnumerator, ResetEnumerator method [Windows Shell], ResetEnumerator method [Windows Shell],IAutoCompleteDropDown interface, _shell_IAutoCompleteDropDown_ResetEnumerator, shell.IAutoCompleteDropDown_ResetEnumerator, shobjidl/IAutoCompleteDropDown::ResetEnumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VPWATERMARKFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Browseui.dll
api_name:
 - IAutoCompleteDropDown.ResetEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: Browseui.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IAutoCompleteDropDown::ResetEnumerator


## -description


Forces the autocomplete object to refresh its list of suggestions when the list is visible.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The drop-down list is always rebuilt before it is displayed, so there is no reason to use this method unless the drop-down list is currently visible.




## -see-also




<a href="https://msdn.microsoft.com/1f956d61-6a09-464e-bfe8-0b3bcb9ea181">IAutoCompleteDropDown</a>
 

 


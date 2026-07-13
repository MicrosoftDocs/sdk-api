---
UID: NF:uiribbon.IUIFramework.SetModes
title: IUIFramework::SetModes (uiribbon.h)
description: Specifies the application modes to enable.
helpviewer_keywords: ["IUIFramework interface [Windows Ribbon]","SetModes method","IUIFramework.SetModes","IUIFramework::SetModes","SetModes","SetModes method [Windows Ribbon]","SetModes method [Windows Ribbon]","IUIFramework interface","scenicintent_IUIFramework_SetModes","uiribbon/IUIFramework::SetModes","windowsribbon.windowsribbon_iuiframework_setmodes"]
old-location: windowsribbon\windowsribbon_iuiframework_setmodes.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\setmodes.htm
ms.date: 12/05/2018
ms.keywords: IUIFramework interface [Windows Ribbon],SetModes method, IUIFramework.SetModes, IUIFramework::SetModes, SetModes, SetModes method [Windows Ribbon], SetModes method [Windows Ribbon],IUIFramework interface, scenicintent_IUIFramework_SetModes, uiribbon/IUIFramework::SetModes, windowsribbon.windowsribbon_iuiframework_setmodes
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
ms.custom: 19H1
f1_keywords:
 - IUIFramework::SetModes
 - uiribbon/IUIFramework::SetModes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIFramework.SetModes
---

# IUIFramework::SetModes


## -description

Specifies the application modes to enable.

## -parameters

### -param iModes

Type: <b>INT32</b>

A bit mask that identifies the modes.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A mode indicates the functionality required and, therefore, which elements should be displayed (or 
				hidden) at run time, depending on the state or context of an application. For example, network connectivity 
				may directly impact the functionality of an application and require a "Network" mode of 
				network-related commands whenever a connection is detected.
			

Modes are specified for elements in the Ribbon markup and bound to individual controls at run time.
			

Modes can be applied to a Ribbon <a href="/windows/desktop/windowsribbon/windowsribbon-element-tab">Tab</a> and <a href="/windows/desktop/windowsribbon/windowsribbon-element-group">Group</a>. 
				

<div class="alert"><b>Note</b>  Modes can be applied to <a href="/windows/desktop/windowsribbon/windowsribbon-element-button">Button</a>, <a href="/windows/desktop/windowsribbon/windowsribbon-element-splitbutton">SplitButton</a>, and <a href="/windows/desktop/windowsribbon/windowsribbon-element-dropdownbutton">DropDownButton</a> controls when hosted in the left 
				column of the Application Menu. 
				</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework">IUIFramework</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-reference-markup-elements">Markup Elements</a>



<a href="/windows/desktop/windowsribbon/ribbon-applicationmodes">Reconfiguring the Ribbon with Application Modes</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
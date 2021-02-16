---
UID: NF:uiribbon.IUIFramework.SetUICommandProperty
title: IUIFramework::SetUICommandProperty (uiribbon.h)
description: Sets a command property, value, or state.
helpviewer_keywords: ["IUIFramework interface [Windows Ribbon]","SetUICommandProperty method","IUIFramework.SetUICommandProperty","IUIFramework::SetUICommandProperty","SetUICommandProperty","SetUICommandProperty method [Windows Ribbon]","SetUICommandProperty method [Windows Ribbon]","IUIFramework interface","scenicintent_IUIFramework_SetUICommandProperty","uiribbon/IUIFramework::SetUICommandProperty","windowsribbon.windowsribbon_iuiframework_setuicommandproperty"]
old-location: windowsribbon\windowsribbon_iuiframework_setuicommandproperty.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\setuicommandproperty.htm
ms.date: 12/05/2018
ms.keywords: IUIFramework interface [Windows Ribbon],SetUICommandProperty method, IUIFramework.SetUICommandProperty, IUIFramework::SetUICommandProperty, SetUICommandProperty, SetUICommandProperty method [Windows Ribbon], SetUICommandProperty method [Windows Ribbon],IUIFramework interface, scenicintent_IUIFramework_SetUICommandProperty, uiribbon/IUIFramework::SetUICommandProperty, windowsribbon.windowsribbon_iuiframework_setuicommandproperty
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
 - IUIFramework::SetUICommandProperty
 - uiribbon/IUIFramework::SetUICommandProperty
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
 - IUIFramework.SetUICommandProperty
---

# IUIFramework::SetUICommandProperty


## -description

Sets a command property, value, or state.

## -parameters

### -param commandId [in]

Type: <b>UINT32</b>

The ID for the Command, which is specified in the Markup resource file.

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

The property key of the command property, value, or state.

### -param value [in]

Type: <b>PROPVARIANT</b>

The property, value, or state.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, otherwise an error value from the following list.

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</td>
<td>The property, value, or state does not support <b>IUIFramework::SetUICommandProperty</b>. 
					They may support being set through invalidation only.
				</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>The operation failed.</td>
</tr>
</table>

## -remarks

A limited number of property keys can be set using <b>IUIFramework::SetUICommandProperty</b>. For those properties where <b>IUIFramework::SetUICommandProperty</b> returns <b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b>, <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand">IUIFramework::InvalidateUICommand</a> should be used instead.

For more information on how to set a property key for a specific control, see the <a href="/windows/desktop/windowsribbon/windowsribbon-controls-entry">Windows Ribbon Framework Control Library</a> page for that control.

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework">IUIFramework</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
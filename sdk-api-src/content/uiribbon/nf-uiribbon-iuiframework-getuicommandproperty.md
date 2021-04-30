---
UID: NF:uiribbon.IUIFramework.GetUICommandProperty
title: IUIFramework::GetUICommandProperty (uiribbon.h)
description: Retrieves a command property, value, or state.
helpviewer_keywords: ["GetUICommandProperty","GetUICommandProperty method [Windows Ribbon]","GetUICommandProperty method [Windows Ribbon]","IUIFramework interface","IUIFramework interface [Windows Ribbon]","GetUICommandProperty method","IUIFramework.GetUICommandProperty","IUIFramework::GetUICommandProperty","scenicintent_IUIFramework_GetUICommandProperty","uiribbon/IUIFramework::GetUICommandProperty","windowsribbon.windowsribbon_iuiframework_getuicommandproperty"]
old-location: windowsribbon\windowsribbon_iuiframework_getuicommandproperty.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\getuicommandproperty.htm
ms.date: 12/05/2018
ms.keywords: GetUICommandProperty, GetUICommandProperty method [Windows Ribbon], GetUICommandProperty method [Windows Ribbon],IUIFramework interface, IUIFramework interface [Windows Ribbon],GetUICommandProperty method, IUIFramework.GetUICommandProperty, IUIFramework::GetUICommandProperty, scenicintent_IUIFramework_GetUICommandProperty, uiribbon/IUIFramework::GetUICommandProperty, windowsribbon.windowsribbon_iuiframework_getuicommandproperty
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
 - IUIFramework::GetUICommandProperty
 - uiribbon/IUIFramework::GetUICommandProperty
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
 - IUIFramework.GetUICommandProperty
---

# IUIFramework::GetUICommandProperty


## -description

Retrieves a command property, value, or state.

## -parameters

### -param commandId [in]

Type: <b>UINT32</b>

The ID for the Command, which is specified in the Markup resource file.

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

The property key of the command property, value, or state.

### -param value [out]

Type: <b>PROPVARIANT*</b>

When this method returns, contains the property, value, or state.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful; otherwise, an error value from the following list.
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</td>
<td>The property, value, or state does not support <b>IUIFramework::GetUICommandProperty</b>. 
					
				</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>The operation failed.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework">IUIFramework</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
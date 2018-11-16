---
UID: NF:uiribbon.IUIFramework.SetUICommandProperty
title: IUIFramework::SetUICommandProperty
author: windows-sdk-content
description: Sets a command property, value, or state.
old-location: windowsribbon\windowsribbon_iuiframework_setuicommandproperty.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiframework\setuicommandproperty.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUIFramework interface [Windows Ribbon],SetUICommandProperty method, IUIFramework.SetUICommandProperty, IUIFramework::SetUICommandProperty, SetUICommandProperty, SetUICommandProperty method [Windows Ribbon], SetUICommandProperty method [Windows Ribbon],IUIFramework interface, scenicintent_IUIFramework_SetUICommandProperty, uiribbon/IUIFramework::SetUICommandProperty, windowsribbon.windowsribbon_iuiframework_setuicommandproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUIFramework.SetUICommandProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiribbon.h
: 
- IUIFramework.SetUICommandProperty
: 
req.product: Windows UI
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



A limited number of property keys can be set using <b>IUIFramework::SetUICommandProperty</b>. For those properties where <b>IUIFramework::SetUICommandProperty</b> returns <b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b>, <a href="https://msdn.microsoft.com/6f6f6815-5523-42d9-a6b2-a21dd26756c0">IUIFramework::InvalidateUICommand</a> should be used instead.

For more information on how to set a property key for a specific control, see the <a href="https://msdn.microsoft.com/bda13e51-7e5f-4600-a6bd-9388bffd6ce2">Windows Ribbon Framework Control Library</a> page for that control.




## -see-also




<a href="https://msdn.microsoft.com/a9b8a30d-dd00-4088-a588-304fde97b84e">IUIFramework</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 


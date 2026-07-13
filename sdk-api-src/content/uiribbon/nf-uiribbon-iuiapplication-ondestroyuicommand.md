---
UID: NF:uiribbon.IUIApplication.OnDestroyUICommand
title: IUIApplication::OnDestroyUICommand (uiribbon.h)
description: Called for each Command specified in the Windows Ribbon framework markup when the application window is destroyed.
helpviewer_keywords: ["IUIApplication interface [Windows Ribbon]","OnDestroyUICommand method","IUIApplication.OnDestroyUICommand","IUIApplication::OnDestroyUICommand","OnDestroyUICommand","OnDestroyUICommand method [Windows Ribbon]","OnDestroyUICommand method [Windows Ribbon]","IUIApplication interface","scenicintent_IUIApplication_OnDestroyUICommand","uiribbon/IUIApplication::OnDestroyUICommand","windowsribbon.windowsribbon_iuiapplication_ondestroyuicommand"]
old-location: windowsribbon\windowsribbon_iuiapplication_ondestroyuicommand.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiapplication\ondestroyuicommand.htm
ms.date: 12/05/2018
ms.keywords: IUIApplication interface [Windows Ribbon],OnDestroyUICommand method, IUIApplication.OnDestroyUICommand, IUIApplication::OnDestroyUICommand, OnDestroyUICommand, OnDestroyUICommand method [Windows Ribbon], OnDestroyUICommand method [Windows Ribbon],IUIApplication interface, scenicintent_IUIApplication_OnDestroyUICommand, uiribbon/IUIApplication::OnDestroyUICommand, windowsribbon.windowsribbon_iuiapplication_ondestroyuicommand
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
 - IUIApplication::OnDestroyUICommand
 - uiribbon/IUIApplication::OnDestroyUICommand
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
 - IUIApplication.OnDestroyUICommand
---

# IUIApplication::OnDestroyUICommand


## -description

Called for each Command specified in the Windows Ribbon framework markup when the application window is destroyed.

## -parameters

### -param commandId [in]

Type: <b>UINT32</b>

The ID for the Command,  which is specified in the markup resource file.

### -param typeID [in]

Type: <b><a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype">UI_COMMANDTYPE</a></b>

The <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype">Command type</a> that is associated with a specific control.

### -param commandHandler [in, optional]

Type: <b><a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler">IUICommandHandler</a>*</b>

A pointer to an <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler">IUICommandHandler</a> object. This value can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This callback notification is sent by the Ribbon framework to the host application for each Command declaration in the markup resource file.
			

All resources in the host application associated with each Command are released.


#### Examples



The following example demonstrates a basic implementation of the <b>IUIApplication::OnDestroyUICommand</b> method.


```cpp
//
//  FUNCTION:    OnDestroyUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler*)
//
//  PURPOSE:    Called for each Command specified in the Ribbon markup 
//                when the Ribbon host application window is destroyed.
//
//  PARAMETERS:    
//                nCmdID - The Command identifier. 
//                typeID - The Command type. 
//                commandHandler - The Command handler. 
//
//  COMMENTS:
//
//
STDMETHODIMP CApplication::OnDestroyUICommand(
    UINT32 nCmdID,
    UI_COMMANDTYPE typeID,
    IUICommandHandler* commandHandler)
{
    return E_NOTIMPL;
}

```


<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication">IUIApplication</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
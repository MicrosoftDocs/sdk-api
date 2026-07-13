---
UID: NF:uiribbon.IUICommandHandler.Execute
title: IUICommandHandler::Execute (uiribbon.h)
description: Responds to execute events on Commands bound to the Command handler.
helpviewer_keywords: ["Execute","Execute method [Windows Ribbon]","Execute method [Windows Ribbon]","IUICommandHandler interface","IUICommandHandler interface [Windows Ribbon]","Execute method","IUICommandHandler.Execute","IUICommandHandler::Execute","scenicintent_IUICommandHandler_Execute","uiribbon/IUICommandHandler::Execute","windowsribbon.windowsribbon_iuicommandhandler_execute"]
old-location: windowsribbon\windowsribbon_iuicommandhandler_execute.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicommandhandler\execute.htm
ms.date: 12/05/2018
ms.keywords: Execute, Execute method [Windows Ribbon], Execute method [Windows Ribbon],IUICommandHandler interface, IUICommandHandler interface [Windows Ribbon],Execute method, IUICommandHandler.Execute, IUICommandHandler::Execute, scenicintent_IUICommandHandler_Execute, uiribbon/IUICommandHandler::Execute, windowsribbon.windowsribbon_iuicommandhandler_execute
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
 - IUICommandHandler::Execute
 - uiribbon/IUICommandHandler::Execute
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
 - IUICommandHandler.Execute
---

# IUICommandHandler::Execute


## -description

Responds to execute events on Commands bound to the Command handler.

## -parameters

### -param commandId [in]

Type: <b>UINT32</b>

The ID for the Command, which is specified in the Markup resource file.

### -param verb [in]

Type: <b><a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb">UI_EXECUTIONVERB</a></b>

The <a href="/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb">UI_EXECUTIONVERB</a> or action that is initiated by the user.

### -param key [in, optional]

Type: <b>const PROPERTYKEY*</b>

A pointer to a <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties">Property Key</a> that has changed value. This parameter can be <b>NULL</b>.

### -param currentValue [in, optional]

Type: <b>const PROPVARIANT*</b>

A pointer to the current value for <i>key</i>. This parameter can be <b>NULL</b>.

### -param commandExecutionProperties [in, optional]

Type: <b><a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset">IUISimplePropertySet</a>*</b>

A pointer to an <a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset">IUISimplePropertySet</a> object that contains 
					Command state properties and property values, such as screen coordinates and list item indices. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each Command in a View must be bound to a new or existing Command handler in the host application.

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler">IUICommandHandler</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
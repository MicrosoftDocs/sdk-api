---
UID: NF:uiribbon.IUICommandHandler.UpdateProperty
title: IUICommandHandler::UpdateProperty (uiribbon.h)
description: Responds to property update requests from the Windows Ribbon framework.
helpviewer_keywords: ["IUICommandHandler interface [Windows Ribbon]","UpdateProperty method","IUICommandHandler.UpdateProperty","IUICommandHandler::UpdateProperty","UpdateProperty","UpdateProperty method [Windows Ribbon]","UpdateProperty method [Windows Ribbon]","IUICommandHandler interface","scenicintent_IUICommandHandler_UpdateProperty","uiribbon/IUICommandHandler::UpdateProperty","windowsribbon.windowsribbon_iuicommandhandler_updateproperty"]
old-location: windowsribbon\windowsribbon_iuicommandhandler_updateproperty.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicommandhandler\updateproperty.htm
ms.date: 12/05/2018
ms.keywords: IUICommandHandler interface [Windows Ribbon],UpdateProperty method, IUICommandHandler.UpdateProperty, IUICommandHandler::UpdateProperty, UpdateProperty, UpdateProperty method [Windows Ribbon], UpdateProperty method [Windows Ribbon],IUICommandHandler interface, scenicintent_IUICommandHandler_UpdateProperty, uiribbon/IUICommandHandler::UpdateProperty, windowsribbon.windowsribbon_iuicommandhandler_updateproperty
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
 - IUICommandHandler::UpdateProperty
 - uiribbon/IUICommandHandler::UpdateProperty
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
 - IUICommandHandler.UpdateProperty
---

# IUICommandHandler::UpdateProperty


## -description

Responds to property update requests from the Windows Ribbon framework.

## -parameters

### -param commandId [in]

Type: <b>UINT32</b>

The ID for the Command, which is specified in the Markup resource file.

### -param key [in]

Type: <b>REFPROPERTYKEY</b>

The <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties">Property Key</a> to update.

### -param currentValue [in, optional]

Type: <b>const PROPVARIANT*</b>

A pointer to the current value for <i>key</i>. This parameter can be <b>NULL</b>.

### -param newValue [out]

Type: <b>PROPVARIANT*</b>

When this method returns, contains a pointer to the new value for 
					<i>key</i>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method should be allowed to return before any subsequent calls to the Ribbon framework are made.

The values of Command properties, such as <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-enabled">UI_PKEY_Enabled</a> or <a href="/windows/desktop/windowsribbon/windowsribbon-reference-properties-uipkey-label">UI_PKEY_Label</a>, are set through calls to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty">SetUICommandProperty</a> or <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand">InvalidateUICommand</a>.

## -see-also

<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler">IUICommandHandler</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-samples-entry">Windows Ribbon Framework Samples</a>
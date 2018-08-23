---
UID: NF:uiribbon.IUICommandHandler.UpdateProperty
title: IUICommandHandler::UpdateProperty
author: windows-sdk-content
description: Responds to property update requests from the Windows Ribbon framework.
old-location: windowsribbon\windowsribbon_iuicommandhandler_updateproperty.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicommandhandler\updateproperty.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IUICommandHandler interface [Windows Ribbon],UpdateProperty method, IUICommandHandler.UpdateProperty, IUICommandHandler::UpdateProperty, UpdateProperty, UpdateProperty method [Windows Ribbon], UpdateProperty method [Windows Ribbon],IUICommandHandler interface, scenicintent_IUICommandHandler_UpdateProperty, uiribbon/IUICommandHandler::UpdateProperty, windowsribbon.windowsribbon_iuicommandhandler_updateproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: UI_VIEWVERB
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUICommandHandler.UpdateProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
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

The <a href="https://msdn.microsoft.com/en-us/library/Dd371196(v=VS.85).aspx">Property Key</a> to update.
				


### -param currentValue [in, optional]

Type: <b>const PROPVARIANT*</b>

A pointer to the current value for <i>key</i>. This parameter can be <b>NULL</b>.
				


### -param newValue [out]

Type: <b>PROPVARIANT*</b>

When this method returns, contains a pointer to the new value for 
					<i>key</i>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method should be allowed to return before any subsequent calls to the Ribbon framework are made.

The values of Command properties, such as <a href="https://msdn.microsoft.com/en-us/library/Dd940400(v=VS.85).aspx">UI_PKEY_Enabled</a> or <a href="https://msdn.microsoft.com/en-us/library/Dd371287(v=VS.85).aspx">UI_PKEY_Label</a>, are set through calls to <a href="https://msdn.microsoft.com/en-us/library/Dd371478(v=VS.85).aspx">SetUICommandProperty</a> or <a href="https://msdn.microsoft.com/en-us/library/Dd371375(v=VS.85).aspx">InvalidateUICommand</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd371491(v=VS.85).aspx">IUICommandHandler</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 


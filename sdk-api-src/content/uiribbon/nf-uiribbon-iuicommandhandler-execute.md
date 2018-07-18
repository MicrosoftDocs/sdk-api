---
UID: NF:uiribbon.IUICommandHandler.Execute
title: IUICommandHandler::Execute
author: windows-sdk-content
description: Responds to execute events on Commands bound to the Command handler.
old-location: windowsribbon\windowsribbon_iuicommandhandler_execute.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicommandhandler\execute.htm
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Execute, Execute method [Windows Ribbon], Execute method [Windows Ribbon],IUICommandHandler interface, IUICommandHandler interface [Windows Ribbon],Execute method, IUICommandHandler.Execute, IUICommandHandler::Execute, scenicintent_IUICommandHandler_Execute, uiribbon/IUICommandHandler::Execute, windowsribbon.windowsribbon_iuicommandhandler_execute
ms.prod: windows
ms.technology: windows-sdk
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
 - IUICommandHandler.Execute
product: Windows
targetos: Windows
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUICommandHandler::Execute


## -description


Responds to execute events on Commands bound to the Command handler.  


## -parameters




### -param commandId [in]

Type: <b>UINT32</b>


					The ID for the Command, which is specified in the Markup resource file.
				


### -param verb [in]

Type: <b><a href="https://msdn.microsoft.com/library/Dd371563(v=VS.85).aspx">UI_EXECUTIONVERB</a></b>


					The <a href="https://msdn.microsoft.com/library/Dd371563(v=VS.85).aspx">UI_EXECUTIONVERB</a> or action that is initiated by the user.
				


### -param key [in, optional]

Type: <b>const PROPERTYKEY*</b>


					A pointer to a <a href="https://msdn.microsoft.com/library/Dd371196(v=VS.85).aspx">Property Key</a> that has changed value. This parameter can be <b>NULL</b>.
				


### -param currentValue [in, optional]

Type: <b>const PROPVARIANT*</b>


					A pointer to the current value for <i>key</i>. This parameter can be <b>NULL</b>.
				


### -param commandExecutionProperties [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/Dd371358(v=VS.85).aspx">IUISimplePropertySet</a>*</b>


					A pointer to an <a href="https://msdn.microsoft.com/library/Dd371358(v=VS.85).aspx">IUISimplePropertySet</a> object that contains 
					Command state properties and property values, such as screen coordinates and list item indices. This parameter can be <b>NULL</b>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each Command in a View must be bound to a new or existing Command handler in the host application.




## -see-also




<a href="https://msdn.microsoft.com/library/Dd371491(v=VS.85).aspx">IUICommandHandler</a>



<a href="https://msdn.microsoft.com/library/Dd371192(v=VS.85).aspx">Windows Ribbon Framework Samples</a>
 

 


---
UID: NF:uiribbon.IUIApplication.OnDestroyUICommand
title: IUIApplication::OnDestroyUICommand
author: windows-sdk-content
description: Called for each Command specified in the Windows Ribbon framework markup when the application window is destroyed.
old-location: windowsribbon\windowsribbon_iuiapplication_ondestroyuicommand.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuiapplication\ondestroyuicommand.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IUIApplication interface [Windows Ribbon],OnDestroyUICommand method, IUIApplication.OnDestroyUICommand, IUIApplication::OnDestroyUICommand, OnDestroyUICommand, OnDestroyUICommand method [Windows Ribbon], OnDestroyUICommand method [Windows Ribbon],IUIApplication interface, scenicintent_IUIApplication_OnDestroyUICommand, uiribbon/IUIApplication::OnDestroyUICommand, windowsribbon.windowsribbon_iuiapplication_ondestroyuicommand
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
 - IUIApplication.OnDestroyUICommand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Windows UI
---

# IUIApplication::OnDestroyUICommand


## -description


Called for each Command specified in the Windows Ribbon framework markup when the application window is destroyed.
		


## -parameters




### -param commandId [in]

Type: <b>UINT32</b>

The ID for the Command,  which is specified in the markup resource file.
				


### -param typeID [in]

Type: <b><a href="https://msdn.microsoft.com/afc2cf3e-c04d-45e1-93b3-23e5966b980c">UI_COMMANDTYPE</a></b>

The <a href="https://msdn.microsoft.com/afc2cf3e-c04d-45e1-93b3-23e5966b980c">Command type</a> that is associated with a specific control.
				


### -param commandHandler [in, optional]

Type: <b><a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a> object. This value can be <b>NULL</b>. 
					


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This callback notification is sent by the Ribbon framework to the host application for each Command declaration in the markup resource file.
			

All resources in the host application associated with each Command are released.


#### Examples



The following example demonstrates a basic implementation of the <b>IUIApplication::OnDestroyUICommand</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
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
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0df1d890-cc78-4375-a17e-6fe7c0249107">IUIApplication</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 


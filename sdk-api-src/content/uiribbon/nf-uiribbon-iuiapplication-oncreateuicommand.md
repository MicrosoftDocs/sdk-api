---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IUIApplication::OnCreateUICommand


## -description



			Called for each Command specified in the Windows Ribbon framework markup to bind the Command to an <a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a>.
		


## -parameters




### -param commandId [in]

Type: <b>UINT32</b>


					The ID for the Command, which is specified in the markup resource file.
				


### -param typeID [in]

Type: <b><a href="https://msdn.microsoft.com/afc2cf3e-c04d-45e1-93b3-23e5966b980c">UI_COMMANDTYPE</a></b>


					The <a href="https://msdn.microsoft.com/afc2cf3e-c04d-45e1-93b3-23e5966b980c">Command type</a> that is associated with a specific control.
				


### -param commandHandler [out]

Type: <b><a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a>**</b>


					When this method returns, contains the address of a pointer to an 
					<a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a> object. This object is a host application 
					Command handler that is bound to one or more Commands.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




				This callback notification is sent by the Ribbon framework to the host application for each Command declaration encountered 
				while processing the markup resource file.


				For each Command specified in the Ribbon markup, the Ribbon framework requires a  Command handler in the host application. 
				A new or existing handler must be assigned to each Command. 
			


#### Examples



The following example demonstrates a basic implementation of the <b>IUIApplication::OnCreateUICommand</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//
//  FUNCTION: OnCreateUICommand(UINT, UI_COMMANDTYPE, IUICommandHandler)
//
//  PURPOSE: Called by the Ribbon framework for each command specified in markup to allow
//           the host application to bind a command handler to that command.
//
//  PARAMETERS:    
//                nCmdID - The Command identifier. 
//                typeID - The Command type. 
//                ppCommandHandler - Pointer to the address of the Command handler. 
//
//  COMMENTS:
//
//    For this sample, return the same command handler for all commands
//    specified in the .xml file.
//    
//
STDMETHODIMP CApplication::OnCreateUICommand(
    UINT nCmdID,
    UI_COMMANDTYPE typeID,
    IUICommandHandler** ppCommandHandler)
{
    HRESULT hr = E_NOTIMPL;

    switch(typeID)
    {
        case UI_COMMANDTYPE_DECIMAL:
            {
                _cwprintf(L"IUIApplication::OnCreateUICommand called for Spinner.\r\n");
                hr = _spSpinnerSite-&gt;QueryInterface(IID_PPV_ARGS(ppCommandHandler));
                break;
            }
        default:
            {
                _cwprintf(L"IUIApplication::OnCreateUICommand called with CmdID=%u, typeID=%u.\r\n", nCmdID, typeID);
                hr = _spCommandHandler-&gt;QueryInterface(IID_PPV_ARGS(ppCommandHandler));
            }
    }    
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/0df1d890-cc78-4375-a17e-6fe7c0249107">IUIApplication</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 


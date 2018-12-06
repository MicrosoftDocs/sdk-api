---
UID: NF:termmgr.ITTerminalManager.CreateDynamicTerminal
title: ITTerminalManager::CreateDynamicTerminal
author: windows-sdk-content
description: The CreateDynamicTerminal method creates a dynamic terminal of a specified terminal class, media type, and direction.
old-location: tapi3\itterminalmanager_createdynamicterminal.htm
tech.root: tapi
ms.assetid: a6590503-8c95-496d-a35a-1bbb34c728e1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateDynamicTerminal, CreateDynamicTerminal method [TAPI 2.2], CreateDynamicTerminal method [TAPI 2.2],ITTerminalManager interface, ITTerminalManager interface [TAPI 2.2],CreateDynamicTerminal method, ITTerminalManager.CreateDynamicTerminal, ITTerminalManager::CreateDynamicTerminal, _tapi3_itterminalmanager_createdynamicterminal, tapi3.itterminalmanager_createdynamicterminal, termmgr/ITTerminalManager::CreateDynamicTerminal
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: termmgr.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Termmgr.h
api_name:
 - ITTerminalManager.CreateDynamicTerminal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITTerminalManager::CreateDynamicTerminal


## -description


The 
<b>CreateDynamicTerminal</b> method creates a dynamic terminal of a specified terminal class, media type, and direction.


## -parameters




### -param pOuterUnknown [in]

If MSP will aggregate the terminal object, set to IUnknown interface pointer for MSP object. Usually this is set to <b>NULL</b>.


### -param iidTerminalClass [in]

GUID identifying class of terminal to be created.


### -param dwMediaType [in]

Descriptor of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> for stream.


### -param Direction [in]


<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor of the media stream direction for terminal.


### -param htAddress [in]

MSP handle.


### -param ppTerminal [out]

Pointer to 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> interface for new terminal.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>fMessageWaiting</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



When choosing a value for <i>pTerminalClass</i>, the only terminal class GUIDs that can be used are those that correspond to terminals that are "dynamically" created. For example, from all terminal classes currently defined by TAPI3, only the following can be used with CreateTerminal: CLSID_MediaStreamTerminal and CLSID_VideoWindowTerm.

In addition, only those dynamic terminal classes that are supported on this address can be used. The application can discover these values by using 
<a href="https://msdn.microsoft.com/1dcb9163-306b-42fc-afb4-41b33d7e2d40">ITTerminalSupport::EnumerateDynamicTerminalClasses</a> or 
<a href="https://msdn.microsoft.com/258fad5c-6269-45ab-bdc0-d38338f8e515">ITTerminalSupport::get_DynamicTerminalClasses</a>.

The application must obtain the <i>pTerminalClass</i> <b>BSTR</b> in two steps: call <b>StringFromIID</b> to convert the GUID to an <b>LPOLESTR</b>, then call 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to convert the <b>LPOLESTR</b> to a <b>BSTR</b>.

The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>pTerminalClass</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/7e5bd83d-42c5-463c-8ce0-c6f466f60588">ITTerminalManager</a>



<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a>



<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>
 

 


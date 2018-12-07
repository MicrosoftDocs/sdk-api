---
UID: NC:shlobj_core.LPFNDFMCALLBACK
title: LPFNDFMCALLBACK
author: windows-sdk-content
description: LPFNDFMCALLBACK may be altered or unavailable.
old-location: shell\LPFNDFMCALLBACK.htm
tech.root: shell
ms.assetid: a5635196-80de-4db9-9c3a-65f2b241b4a0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LPFNDFMCALLBACK, LPFNDFMCALLBACK callback, LPFNDFMCALLBACK callback function [Windows Shell], _win32_LPFNDFMCALLBACK, shell.LPFNDFMCALLBACK, shlobj_core/LPFNDFMCALLBACK
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - UserDefined
api_location:
 - shlobj_core.h
api_name:
 - LPFNDFMCALLBACK
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPFNDFMCALLBACK callback function


## -description


<p class="CCE_Message">[<b>LPFNDFMCALLBACK</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Defines the prototype for the callback function that receives messages from the Shell's default context menu implementation.


## -parameters




### -param *psf [in, optional]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> object the message applies to. This value can be <b>NULL</b>.


### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the window that contains the view. This value can be <b>NULL</b>.


### -param *pdtobj [in, optional]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>


<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> that represents the selection the context menu is based on. This value can be <b>NULL</b>.


### -param uMsg

Type: <b>UINT</b>

One of the following notifications.
    					
                        

<table class="clsStd">
<tr>
<th>Notification</th>
<th>Usage</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2fd779ac-7dd6-4b81-86dc-8930db27ae59">DFM_MERGECONTEXTMENU</a>
</td>
<td>Sent by the default context menu implementation to allow <b>LPFNDFMCALLBACK</b> to add items to the menu.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/bd3200a6-b9e7-414c-9a01-c432cb306dba">DFM_INVOKECOMMAND</a>
</td>
<td>Sent by the default context menu implementation to request <b>LPFNDFMCALLBACK</b> to invoke a menu command.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9e4ad96e-7c90-456e-8668-21b347f2915c">DFM_GETDEFSTATICID</a>
</td>
<td>Sent by the default context menu implementation when the default menu command is being created, allowing an alternate choice to be made.</td>
</tr>
</table>
 


### -param wParam

Type: <b>WPARAM</b>

Additional information. See the individual notification pages for specific requirements.


### -param lParam

Type: <b>LPARAM</b>

Additional information. See the individual notification pages for specific requirements.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if the message was handled, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The message was not handled.

</td>
</tr>
</table>
 




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

# IContextMenuCB::CallBack


## -description


Enables the callback function for a context menu.


## -parameters




### -param psf [in]

Type: <b><a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/35190a72-298b-4554-b924-e1357b583a99">IShellFolder</a> interface of the object that supports the <b>IContextMenuCB::CallBack</b> interface. The context menu interface is returned on a call to <a href="https://msdn.microsoft.com/ec863dbf-8ec9-4952-8912-575125e6dd09">GetUIObjectOf</a>.


### -param hwndOwner [in, optional]

Type: <b>HWND</b>

A handle to the owner of the context menu. This value can be <b>NULL</b>.


### -param pdtobj [in]

Type: <b><a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> that contains information about a menu selection. Implement interface <b>IDataObject</b>, or call <a href="https://msdn.microsoft.com/d56cdafe-9463-43a5-8ef0-6cfaf0c524a8">SHCreateDataObject</a> for the default implementation.


### -param uMsg [in]

Type: <b>UINT</b>

A notification from the Shell's default menu implementation. For example, the default menu implementation calls <a href="https://msdn.microsoft.com/2fd779ac-7dd6-4b81-86dc-8930db27ae59">DFM_MERGECONTEXTMENU</a> to allow the implementer of <b>IContextMenuCB::CallBack</b> to remove, add, or disable context menu items in this callback. Use one of the following notifications.

                    


<table class="clsStd">
<tr>
<td>
<a href="https://msdn.microsoft.com/2fd779ac-7dd6-4b81-86dc-8930db27ae59">DFM_MERGECONTEXTMENU</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/bd3200a6-b9e7-414c-9a01-c432cb306dba">DFM_INVOKECOMMAND</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/40ed981b-6d03-4c4f-9e70-1a01d49edcb0">DFM_GETHELPTEXT</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/85bdd1d0-5b68-44a5-a1b0-4845b5be34d0">DFM_GETHELPTEXTW</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4584a3da-6c92-4ecd-8cf2-e4afc1b8321d">DFM_WM_MEASUREITEM</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2515bbab-025f-4f00-8564-a732d68edea3">DFM_WM_DRAWITEM</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/314e83f7-839d-4ca0-b5c1-842c5bf14923">DFM_WM_INITMENUPOPUP</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/97ff3cdf-ed0c-4813-8d5a-b5141636d32c">DFM_VALIDATECMD</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6ef885e5-2ddd-4a1b-9f8e-016a74e292b1">DFM_INVOKECOMMANDEX</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8aa764f7-d5d4-4a84-94d2-993265e1eb5a">DFM_MAPCOMMANDNAME</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/9e4ad96e-7c90-456e-8668-21b347f2915c">DFM_GETDEFSTATICID</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/bd12a38e-4d50-43ad-9d1f-8fefa90b44f9">DFM_GETVERB</a>
</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/37414335-4f3c-461e-bd05-d6ef850f972a">DFM_MERGECONTEXTMENU_BOTTOM</a>
</td>
</tr>
</table>
 




### -param wParam [in]

Type: <b>WPARAM</b>

Data specific to the notification specified in <i>uMsg</i>. See the individual notification page for specific requirements.


### -param lParam [in]

Type: <b>LPARAM</b>

Data specific to the notification specified in <i>uMsg</i>. See the individual notification page for specific requirements.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cff79cdc-8a01-4575-9af7-2a485c6a8e46">Creating Context Menu Handlers</a>



<a href="https://msdn.microsoft.com/1a4c183b-97cf-4c9a-af5a-bcea7c2755a5">IContextMenuCB</a>
 

 


---
UID: NF:strmif.IDvdControl2.ShowMenu
title: IDvdControl2::ShowMenu
author: windows-sdk-content
description: The ShowMenu method displays the specified menu, if available.
old-location: dshow\idvdcontrol2_showmenu.htm
tech.root: DirectShow
ms.assetid: 7427ff6c-875b-40ce-aa96-3d32b607dc56
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IDvdControl2 interface [DirectShow],ShowMenu method, IDvdControl2.ShowMenu, IDvdControl2::ShowMenu, IDvdControl2ShowMenu, ShowMenu, ShowMenu method [DirectShow], ShowMenu method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_showmenu, strmif/IDvdControl2::ShowMenu
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.ShowMenu
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::ShowMenu


## -description



The <code>ShowMenu</code> method displays the specified menu, if available.




## -parameters




### -param MenuID [in]

A <a href="https://msdn.microsoft.com/2fd107d7-7531-4bce-89b9-b44388b47b91">DVD_MENU_ID</a> enumeration value that specifies the menu to display.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://msdn.microsoft.com/05eb5ab8-a1b3-4876-bac3-29510af8cdbd">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>MenuID</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_INVALIDDOMAIN</b></dt>
</dl>
</td>
<td width="60%">
Invalid domain.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_MENU_DOES_NOT_EXIST</b></dt>
</dl>
</td>
<td width="60%">
The specified menu does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>
 




## -remarks



The Video Manager Menu (VMGM) should be accessible from the Title or the Video Title Set domains. The Video Title Set menus (VTSMs) might only be accessible through the VMGM. Any submenus under each VTSM (for chapters, angles, and audio and subpicture streams) are only accessible through that VTSM.

This method is demonstrated in the DVDSample application application in <b>CDvdCore::RootMenu</b> and <b>CDvdCore::TitleMenu</b>.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Menu_Call</td>
<td>All.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>



<a href="https://msdn.microsoft.com/8c5f8072-b74f-4e15-8991-73bcc4145fd2">Working With DVD Menus</a>
 

 


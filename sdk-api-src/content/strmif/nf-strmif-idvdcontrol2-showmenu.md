---
UID: NF:strmif.IDvdControl2.ShowMenu
title: IDvdControl2::ShowMenu (strmif.h)
description: The ShowMenu method displays the specified menu, if available.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","ShowMenu method","IDvdControl2.ShowMenu","IDvdControl2::ShowMenu","IDvdControl2ShowMenu","ShowMenu","ShowMenu method [DirectShow]","ShowMenu method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_showmenu","strmif/IDvdControl2::ShowMenu"]
old-location: dshow\idvdcontrol2_showmenu.htm
tech.root: DirectShow
ms.assetid: 7427ff6c-875b-40ce-aa96-3d32b607dc56
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],ShowMenu method, IDvdControl2.ShowMenu, IDvdControl2::ShowMenu, IDvdControl2ShowMenu, ShowMenu, ShowMenu method [DirectShow], ShowMenu method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_showmenu, strmif/IDvdControl2::ShowMenu
f1_keywords:
- strmif/IDvdControl2.ShowMenu
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::ShowMenu


## -description



The <code>ShowMenu</code> method displays the specified menu, if available.




## -parameters




### -param MenuID [in]

A <a href="https://docs.microsoft.com/windows/win32/api/strmif/ne-strmif-dvd_menu_id">DVD_MENU_ID</a> enumeration value that specifies the menu to display.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_cmd_flags">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command.


### -param ppCmd [out]

Receives a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcmd">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>
 

 


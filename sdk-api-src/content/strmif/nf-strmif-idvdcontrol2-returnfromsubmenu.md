---
UID: NF:strmif.IDvdControl2.ReturnFromSubmenu
title: IDvdControl2::ReturnFromSubmenu (strmif.h)
description: The ReturnFromSubmenu method returns the display from a submenu to its parent menu.
helpviewer_keywords: ["IDvdControl2 interface [DirectShow]","ReturnFromSubmenu method","IDvdControl2.ReturnFromSubmenu","IDvdControl2::ReturnFromSubmenu","IDvdControl2ReturnFromSubmenu","ReturnFromSubmenu","ReturnFromSubmenu method [DirectShow]","ReturnFromSubmenu method [DirectShow]","IDvdControl2 interface","dshow.idvdcontrol2_returnfromsubmenu","strmif/IDvdControl2::ReturnFromSubmenu"]
old-location: dshow\idvdcontrol2_returnfromsubmenu.htm
tech.root: dshow
ms.assetid: ef213ab6-3993-46e4-803d-3ce195256e7e
ms.date: 12/05/2018
ms.keywords: IDvdControl2 interface [DirectShow],ReturnFromSubmenu method, IDvdControl2.ReturnFromSubmenu, IDvdControl2::ReturnFromSubmenu, IDvdControl2ReturnFromSubmenu, ReturnFromSubmenu, ReturnFromSubmenu method [DirectShow], ReturnFromSubmenu method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_returnfromsubmenu, strmif/IDvdControl2::ReturnFromSubmenu
f1_keywords:
- strmif/IDvdControl2.ReturnFromSubmenu
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
- IDvdControl2.ReturnFromSubmenu
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl2::ReturnFromSubmenu


## -description



The <code>ReturnFromSubmenu</code> method returns the display from a submenu to its parent menu.




## -parameters




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
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_NO_GOUP_PGC</b></dt>
</dl>
</td>
<td width="60%">
The operation cannot be performed because no GoUp program chain (PGC) is available.

</td>
</tr>
</table>
 




## -remarks



If the DVD Navigator is at the top-level menu, this method calls the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol2-resume">IDvdControl2::Resume</a> method so that play continues where it left off.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>GoUP</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/synchronizing-dvd-commands">Synchronizing DVD Commands</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/working-with-dvd-menus">Working With DVD Menus</a>
 

 


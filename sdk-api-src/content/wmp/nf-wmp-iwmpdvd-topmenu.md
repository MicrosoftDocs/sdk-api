---
UID: NF:wmp.IWMPDVD.topMenu
title: IWMPDVD::topMenu (wmp.h)
description: The topMenu method stops playback and displays the top (or root) menu for the current title.
helpviewer_keywords: ["IWMPDVD interface [Windows Media Player]","topMenu method","IWMPDVD.topMenu","IWMPDVD::topMenu","IWMPDVDtopMenu","topMenu","topMenu method [Windows Media Player]","topMenu method [Windows Media Player]","IWMPDVD interface","wmp.iwmpdvd_topmenu","wmp/IWMPDVD::topMenu"]
old-location: wmp\iwmpdvd_topmenu.htm
tech.root: WMP
ms.assetid: 5b96763f-a174-45df-b988-955f9619a4c1
ms.date: 12/05/2018
ms.keywords: IWMPDVD interface [Windows Media Player],topMenu method, IWMPDVD.topMenu, IWMPDVD::topMenu, IWMPDVDtopMenu, topMenu, topMenu method [Windows Media Player], topMenu method [Windows Media Player],IWMPDVD interface, wmp.iwmpdvd_topmenu, wmp/IWMPDVD::topMenu
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPDVD::topMenu
 - wmp/IWMPDVD::topMenu
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPDVD.topMenu
---

# IWMPDVD::topMenu


## -description

The <b>topMenu</b> method stops playback and displays the top (or root) menu for the current title.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

Every DVD is authored differently. The DVD must contain a menu for this method to work. Some DVDs are authored so that the <b>topMenu</b> and <b>IWMPDVD::titleMenu</b> methods open the same menu. The <b>topMenu</b> method usually invokes the top (or root) menu, but it may invoke the title menu if there is no root menu available.

<b>Windows Media Player 10 Mobile: </b>This method always returns S_OK, but does not perform the intended operation.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpdvd-titlemenu">IWMPDVD::titleMenu</a>

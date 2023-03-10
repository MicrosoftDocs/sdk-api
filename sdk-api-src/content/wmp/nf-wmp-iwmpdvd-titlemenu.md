---
UID: NF:wmp.IWMPDVD.titleMenu
title: IWMPDVD::titleMenu (wmp.h)
description: The titleMenu method stops playback and displays the title menu.
helpviewer_keywords: ["IWMPDVD interface [Windows Media Player]","titleMenu method","IWMPDVD.titleMenu","IWMPDVD::titleMenu","IWMPDVDtitleMenu","titleMenu","titleMenu method [Windows Media Player]","titleMenu method [Windows Media Player]","IWMPDVD interface","wmp.iwmpdvd_titlemenu","wmp/IWMPDVD::titleMenu"]
old-location: wmp\iwmpdvd_titlemenu.htm
tech.root: WMP
ms.assetid: 93a06367-5b0b-421d-abef-f6cd23e5b0d5
ms.date: 12/05/2018
ms.keywords: IWMPDVD interface [Windows Media Player],titleMenu method, IWMPDVD.titleMenu, IWMPDVD::titleMenu, IWMPDVDtitleMenu, titleMenu, titleMenu method [Windows Media Player], titleMenu method [Windows Media Player],IWMPDVD interface, wmp.iwmpdvd_titlemenu, wmp/IWMPDVD::titleMenu
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
 - IWMPDVD::titleMenu
 - wmp/IWMPDVD::titleMenu
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
 - IWMPDVD.titleMenu
---

# IWMPDVD::titleMenu


## -description

The <b>titleMenu</b> method stops playback and displays the title menu.



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

Every DVD is authored differently. The DVD must contain a menu for this method to work. Some DVDs are authored so that the <b>IWMPDVD::topMenu</b> and <b>titleMenu</b> methods open the same menu. The <b>titleMenu</b> method usually invokes the title menu, but it may invoke the top menu if there is no title menu available.

<b>Windows Media Player 10 Mobile: </b>This method always returns S_OK, but does not perform the intended operation.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpdvd-topmenu">IWMPDVD::topMenu</a>

---
UID: NF:wmp.IWMPDVD.back
title: IWMPDVD::back (wmp.h)
description: The back method returns the display from a submenu to its parent menu.
helpviewer_keywords: ["IWMPDVD interface [Windows Media Player]","back method","IWMPDVD.back","IWMPDVD::back","IWMPDVDback","back","back method [Windows Media Player]","back method [Windows Media Player]","IWMPDVD interface","wmp.iwmpdvd_back","wmp/IWMPDVD::back"]
old-location: wmp\iwmpdvd_back.htm
tech.root: WMP
ms.assetid: 89d3c8e2-4517-45db-a20c-961089ee8845
ms.date: 12/05/2018
ms.keywords: IWMPDVD interface [Windows Media Player],back method, IWMPDVD.back, IWMPDVD::back, IWMPDVDback, back, back method [Windows Media Player], back method [Windows Media Player],IWMPDVD interface, wmp.iwmpdvd_back, wmp/IWMPDVD::back
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
 - IWMPDVD::back
 - wmp/IWMPDVD::back
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
 - IWMPDVD.back
---

# IWMPDVD::back


## -description

The <b>back</b> method returns the display from a submenu to its parent menu.



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

Every DVD is authored differently. Some DVDs are authored so that the <b>back</b> method is available from the root menu, but when invoked, it will do nothing.

<b>Windows Media Player 10 Mobile: </b>This method always returns S_OK, but does not perform the intended operation.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpdvd">IWMPDVD Interface</a>

---
UID: NF:wmp.IWMPControls.put_currentPosition
title: IWMPControls::put_currentPosition (wmp.h)
description: The put_currentPosition method specifies the current position in the media item in seconds from the beginning.
helpviewer_keywords: ["IWMPControls interface [Windows Media Player]","put_currentPosition method","IWMPControls.put_currentPosition","IWMPControls::put_currentPosition","IWMPControlsput_currentPosition","put_currentPosition","put_currentPosition method [Windows Media Player]","put_currentPosition method [Windows Media Player]","IWMPControls interface","wmp.iwmpcontrols_put_currentposition","wmp/IWMPControls::put_currentPosition"]
old-location: wmp\iwmpcontrols_put_currentposition.htm
tech.root: WMP
ms.assetid: 7deedeed-8ce9-4fd7-9825-817204a9cb3e
ms.date: 12/05/2018
ms.keywords: IWMPControls interface [Windows Media Player],put_currentPosition method, IWMPControls.put_currentPosition, IWMPControls::put_currentPosition, IWMPControlsput_currentPosition, put_currentPosition, put_currentPosition method [Windows Media Player], put_currentPosition method [Windows Media Player],IWMPControls interface, wmp.iwmpcontrols_put_currentposition, wmp/IWMPControls::put_currentPosition
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPControls::put_currentPosition
 - wmp/IWMPControls::put_currentPosition
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
 - IWMPControls.put_currentPosition
---

# IWMPControls::put_currentPosition


## -description

The <b>put_currentPosition</b> method specifies the current position in the media item in seconds from the beginning.

## -parameters

### -param dCurrentPosition [in]

<b>double</b> containing the current position.

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

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpcontrols-get_currentposition">IWMPControls::get_currentPosition</a>
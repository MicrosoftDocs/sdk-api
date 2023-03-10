---
UID: NF:wmp.IWMPCdromBurn.erase
title: IWMPCdromBurn::erase (wmp.h)
description: The erase method erases the current CD.
helpviewer_keywords: ["IWMPCdromBurn interface [Windows Media Player]","erase method","IWMPCdromBurn.erase","IWMPCdromBurn::erase","IWMPCdromBurnerase","erase","erase method [Windows Media Player]","erase method [Windows Media Player]","IWMPCdromBurn interface","wmp.iwmpcdromburn_erase","wmp/IWMPCdromBurn::erase"]
old-location: wmp\iwmpcdromburn_erase.htm
tech.root: WMP
ms.assetid: 93a37f59-4269-4f84-93dc-8350aabd4ebe
ms.date: 12/05/2018
ms.keywords: IWMPCdromBurn interface [Windows Media Player],erase method, IWMPCdromBurn.erase, IWMPCdromBurn::erase, IWMPCdromBurnerase, erase, erase method [Windows Media Player], erase method [Windows Media Player],IWMPCdromBurn interface, wmp.iwmpcdromburn_erase, wmp/IWMPCdromBurn::erase
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
 - IWMPCdromBurn::erase
 - wmp/IWMPCdromBurn::erase
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
 - IWMPCdromBurn.erase
---

# IWMPCdromBurn::erase


## -description

The <b>erase</b> method erases the current CD.



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

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

This method will not work if the disc in the drive is not rewritable. Use <a href="/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable">IWMPCdromBurn::isAvailable</a> to determine whether a CD can be erased.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn">IWMPCdromBurn Interface</a>

---
UID: NN:bdaiface.IBDA_AutoDemodulate
title: IBDA_AutoDemodulate (bdaiface.h)
description: If a BDA device filter, specifically a demodulator, exposes this interface, it indicates that the filter can automatically detect signal characteristics.
helpviewer_keywords: ["IBDA_AutoDemodulate","IBDA_AutoDemodulate interface [Microsoft TV Technologies]","IBDA_AutoDemodulate interface [Microsoft TV Technologies]","described","IBDA_AutoDemodulateInterface","bdaiface/IBDA_AutoDemodulate","mstv.ibda_autodemodulate"]
old-location: mstv\ibda_autodemodulate.htm
tech.root: mstv
ms.assetid: 91588290-bae9-4c6d-9ec7-5d3777208e2a
ms.date: 12/05/2018
ms.keywords: IBDA_AutoDemodulate, IBDA_AutoDemodulate interface [Microsoft TV Technologies], IBDA_AutoDemodulate interface [Microsoft TV Technologies],described, IBDA_AutoDemodulateInterface, bdaiface/IBDA_AutoDemodulate, mstv.ibda_autodemodulate
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_AutoDemodulate
 - bdaiface/IBDA_AutoDemodulate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_AutoDemodulate
---

# IBDA_AutoDemodulate interface


## -description

If a BDA device filter, specifically a demodulator, exposes this interface, it indicates that the filter can automatically detect signal characteristics. With this information, the Network Provider can be more efficient in managing the tuning process. For more information, see <b>KSPROPSETID_BdaAutodemodulate</b> in the Windows DDK.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_AutoDemodulate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_AutoDemodulate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_AutoDemodulate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_autodemodulate-put_autodemodulate">put_AutoDemodulate</a>
</td>
<td align="left" width="63%">
Instructs the BDA device filter to automatically detect signal characteristics.

</td>
</tr>
</table>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_AutoDemodulate)</code>.

## -see-also

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>


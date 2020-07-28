---
UID: NN:bdatif.IBDA_TIF_REGISTRATION
title: IBDA_TIF_REGISTRATION (bdatif.h)
description: The IBDA_TIF_REGISTRATION interface is exposed by the BDA Network Provider.
helpviewer_keywords: ["IBDA_TIF_REGISTRATION","IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies]","IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies]","described","IBDA_TIF_REGISTRATIONInterface","bdatif/IBDA_TIF_REGISTRATION","mstv.ibda_tif_registration"]
old-location: mstv\ibda_tif_registration.htm
tech.root: mstv
ms.assetid: 96c76a81-57c9-4c4b-a5f6-7b9862757847
ms.date: 12/05/2018
ms.keywords: IBDA_TIF_REGISTRATION, IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies], IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies],described, IBDA_TIF_REGISTRATIONInterface, bdatif/IBDA_TIF_REGISTRATION, mstv.ibda_tif_registration
f1_keywords:
- bdatif/IBDA_TIF_REGISTRATION
dev_langs:
- c++
req.header: bdatif.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- bdatif.h
api_name:
- IBDA_TIF_REGISTRATION
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_TIF_REGISTRATION interface


## -description



The <b>IBDA_TIF_REGISTRATION</b> interface is 
         exposed by the BDA Network Provider. It enables a Transport Information Filter (TIF) to register itself with 
         the Network Provider. This interface supersedes the 
         <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nn-bdatif-impeg2_tif_control">IMPEG2_TIF_CONTROL</a> interface.

Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_TIF_REGISTRATION</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_TIF_REGISTRATION</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_TIF_REGISTRATION</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-ibda_tif_registration-registertifex">RegisterTIFEx</a>
</td>
<td align="left" width="63%">
Registers the TIF with the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-ibda_tif_registration-unregistertif">UnregisterTIF</a>
</td>
<td align="left" width="63%">
Unregisters the TIF with the Network Provider.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> 
     operator: <code>__uuidof(IBDA_TIF_REGISTRATION)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 


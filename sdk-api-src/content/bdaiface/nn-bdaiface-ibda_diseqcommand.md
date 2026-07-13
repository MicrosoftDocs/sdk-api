---
UID: NN:bdaiface.IBDA_DiseqCommand
title: IBDA_DiseqCommand (bdaiface.h)
description: Controls cable television satellite equipment, using Digital Satellite Equipment Control (DiSEqC) commands.
helpviewer_keywords: ["IBDA_DiseqCommand","IBDA_DiseqCommand interface [Microsoft TV Technologies]","IBDA_DiseqCommand interface [Microsoft TV Technologies]","described","bdaiface/IBDA_DiseqCommand","mstv.ibda_diseqcommand"]
old-location: mstv\ibda_diseqcommand.htm
tech.root: mstv
ms.assetid: 0148a32d-b131-46ba-bbf0-82e2cf9c7d86
ms.date: 12/05/2018
ms.keywords: IBDA_DiseqCommand, IBDA_DiseqCommand interface [Microsoft TV Technologies], IBDA_DiseqCommand interface [Microsoft TV Technologies],described, bdaiface/IBDA_DiseqCommand, mstv.ibda_diseqcommand
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bdaiface.idl
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
 - IBDA_DiseqCommand
 - bdaiface/IBDA_DiseqCommand
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
 - IBDA_DiseqCommand
---

# IBDA_DiseqCommand interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Controls cable television satellite equipment, using Digital Satellite Equipment Control (DiSEqC) commands.

## -inheritance

The <b>IBDA_DiseqCommand</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_DiseqCommand</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

Depending on the cable television equipment in use, this interface can be used to select the LNB converter source, move a motor dish, or control radio frequency (RF) switching equipment.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DiseqCommand)</code>.

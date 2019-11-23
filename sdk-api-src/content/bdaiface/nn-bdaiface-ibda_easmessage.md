---
UID: NN:bdaiface.IBDA_EasMessage
title: IBDA_EasMessage (bdaiface.h)

description: The IBDA_EasMessage interface represents an ATSC emergency alert system (EAS) message table.
old-location: mstv\ibda_easmessage.htm
tech.root: mstv
ms.assetid: dfacaa47-c844-434f-951a-9ee38fa8af4a

ms.date: 12/05/2018
ms.keywords: IBDA_EasMessage, IBDA_EasMessage interface [Microsoft TV Technologies], IBDA_EasMessage interface [Microsoft TV Technologies],described, IBDA_EasMessageInterface, bdaiface/IBDA_EasMessage, mstv.ibda_easmessage
ms.topic: interface
f1_keywords: 
 - "bdaiface/IBDA_EasMessage"
dev_langs:
 - c++
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - Bdaiface.h
api_name:
 - IBDA_EasMessage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBDA_EasMessage interface


## -description


The <b>IBDA_EasMessage</b> interface represents an ATSC emergency alert system (EAS) message table. This interface is currently implemented on the TIF and registered as a service by the TIF.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_EasMessage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_EasMessage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_EasMessage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bdaiface/nf-bdaiface-ibda_easmessage-get_easmessage">get_EasMessage</a>
</td>
<td align="left" width="63%">
Retrieves an EAS message.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_EasMessage)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 


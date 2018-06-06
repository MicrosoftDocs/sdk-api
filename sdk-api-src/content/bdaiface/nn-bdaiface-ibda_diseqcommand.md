---
UID: NN:bdaiface.IBDA_DiseqCommand
title: IBDA_DiseqCommand
author: windows-sdk-content
description: Controls cable television satelite equipment, using Digital Satellite Equipment Control (DiSEqC) commands.
old-location: mstv\ibda_diseqcommand.htm
old-project: mstv
ms.assetid: 0148a32d-b131-46ba-bbf0-82e2cf9c7d86
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_DiseqCommand, IBDA_DiseqCommand interface [Microsoft TV Technologies], IBDA_DiseqCommand interface [Microsoft TV Technologies],described, bdaiface/IBDA_DiseqCommand, mstv.ibda_diseqcommand
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_DiseqCommand
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_DiseqCommand interface


## -description


Controls cable television satelite equipment, using Digital Satellite Equipment Control (DiSEqC) commands.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_DiseqCommand</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_DiseqCommand</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_DiseqCommand</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed481bfb-dd80-44fa-bf64-a0f8e903ae35">get_DiseqResponse</a>
</td>
<td align="left" width="63%">

            Gets the driver's response to a DiSEqC command.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09ed3d1d-026a-43b3-863b-a77260e082d8">put_DiseqLNBSource</a>
</td>
<td align="left" width="63%">

            Sets the low-noise block (LNB) converter source.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de5cbfa9-1509-47cf-b994-24b5dac76d8e">put_DiseqRepeats</a>
</td>
<td align="left" width="63%">

            Enables or disables repeated DiSEqC commands.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ee77311-0b1d-43b1-af8e-bb886170701d">put_DiseqSendCommand</a>
</td>
<td align="left" width="63%">

            Sends a DiSEqC command.
          

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23523ac9-19e0-4247-a697-24d6f1c07285">put_DiseqUseToneBurst</a>
</td>
<td align="left" width="63%">

            Enables or disables Tone-Burst commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d70f5e3c-bd5d-48cf-b4fd-e1ae2ba66f69">put_EnableDiseqCommands</a>
</td>
<td align="left" width="63%">

            Enables or disables the use of DiSEqC commands.
          

</td>
</tr>
</table> 


## -remarks




        Depending on the cable television equipment in use, this interface can be used to select the LNB converter source, move a motor dish, or control radio frequency (RF) switching equipment.
      

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_DiseqCommand)</code>.




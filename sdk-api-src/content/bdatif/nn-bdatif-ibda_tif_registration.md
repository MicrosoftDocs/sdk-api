---
UID: NN:bdatif.IBDA_TIF_REGISTRATION
title: IBDA_TIF_REGISTRATION
author: windows-sdk-content
description: The IBDA_TIF_REGISTRATION interface is exposed by the BDA Network Provider.
old-location: mstv\ibda_tif_registration.htm
old-project: mstv
ms.assetid: 96c76a81-57c9-4c4b-a5f6-7b9862757847
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_TIF_REGISTRATION, IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies], IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies],described, IBDA_TIF_REGISTRATIONInterface, bdatif/IBDA_TIF_REGISTRATION, mstv.ibda_tif_registration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: SmartCardApplication
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IBDA_TIF_REGISTRATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IBDA_TIF_REGISTRATION interface


## -description



The <b>IBDA_TIF_REGISTRATION</b> interface is 
         exposed by the BDA Network Provider. It enables a Transport Information Filter (TIF) to register itself with 
         the Network Provider. This interface supersedes the 
         <a href="https://msdn.microsoft.com/9583365d-b318-49e2-a32f-f6cc9d3f289d">IMPEG2_TIF_CONTROL</a> interface.

Applications do not use this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_TIF_REGISTRATION</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_TIF_REGISTRATION</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1cfc653f-b552-4f38-9ca1-457ab4de3598">RegisterTIFEx</a>
</td>
<td align="left" width="63%">
Registers the TIF with the Network Provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ba46145-6b77-4577-9611-0e0a155aa308">UnregisterTIF</a>
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




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 


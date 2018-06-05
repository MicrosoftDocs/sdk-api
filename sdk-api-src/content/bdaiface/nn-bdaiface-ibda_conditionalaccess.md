---
UID: NN:bdaiface.IBDA_ConditionalAccess
title: IBDA_ConditionalAccess
author: windows-sdk-content
description: The IBDA_ConditionalAccess interface provides conditional access to program content.
old-location: mstv\ibda_conditionalaccess.htm
old-project: mstv
ms.assetid: 93bd3c38-2591-4d36-b296-5ad939487277
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IBDA_ConditionalAccess, IBDA_ConditionalAccess interface [Microsoft TV Technologies], IBDA_ConditionalAccess interface [Microsoft TV Technologies],described, IBDA_ConditionalAccessInterface, bdaiface/IBDA_ConditionalAccess, mstv.ibda_conditionalaccess
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: UICloseReasonType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bdaiface.h
api_name:
-	IBDA_ConditionalAccess
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IBDA_ConditionalAccess interface


## -description


The <b>IBDA_ConditionalAccess</b> interface provides conditional access to program content.

<b>OCUR Devices: </b>This interface supports OpenCable Unidirectional Cable Receiver (OCUR) devices. See <a href="https://msdn.microsoft.com/7b641b94-9854-4ca8-8362-a9e1e49bbdd2">OCUR Devices</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBDA_ConditionalAccess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBDA_ConditionalAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBDA_ConditionalAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e0e2905-fb7c-4532-be3e-198ca620f894">AddProgram</a>
</td>
<td align="left" width="63%">
Adds a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/361fe0ee-5834-4474-9cc7-92ea9077571c">get_Entitlement</a>
</td>
<td align="left" width="63%">
Retrieves the entitlement type for a virtual channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5667ca9c-c46d-43d6-a7da-1f0ff340e869">get_SmartCardApplications</a>
</td>
<td align="left" width="63%">
Retrieves a list of the smart card applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c9143e7-1e59-4f64-84b8-2bbac18cf787">get_SmartCardInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about the smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/940247b0-c002-414f-9d01-9f4acfe90a35">get_SmartCardStatus</a>
</td>
<td align="left" width="63%">
Retrieves the status of the smart card.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d1856d8-d2e6-4ab1-a1ce-7dcf9bc8bd39">GetModuleUI</a>
</td>
<td align="left" width="63%">
Retrieves a list of the smart card applications.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f9dcd29-ccd9-4154-bf11-932a3635c156">InformUIClosed</a>
</td>
<td align="left" width="63%">
Informs the device that the user-interface dialog is closed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc0d14e8-f4bc-49fe-b63c-0521f5bb3dbb">RemoveProgram</a>
</td>
<td align="left" width="63%">
Removes a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d38fc9bc-70e8-419e-b7be-33d1f53a723e">SetProgram</a>
</td>
<td align="left" width="63%">
Sets a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1241d61d-e16a-4f80-b187-759db316f25b">TuneByChannel</a>
</td>
<td align="left" width="63%">
Tunes to a virtual channel.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof()</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 


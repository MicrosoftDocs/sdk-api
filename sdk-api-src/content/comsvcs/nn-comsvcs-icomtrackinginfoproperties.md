---
UID: NN:comsvcs.IComTrackingInfoProperties
title: IComTrackingInfoProperties
author: windows-sdk-content
description: Retrieves the total number of properties associated with a tracking information object and their names.
old-location: cos\icomtrackinginfoproperties.htm
tech.root: cossdk
ms.assetid: 1964b04e-7146-4d08-a08f-a85393d07592
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IComTrackingInfoProperties, IComTrackingInfoProperties interface [COM+], IComTrackingInfoProperties interface [COM+],described, _dtc_IComTrackingInfoProperties, comsvcs/IComTrackingInfoProperties, cos.icomtrackinginfoproperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IComTrackingInfoProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComTrackingInfoProperties interface


## -description


Retrieves the total number of properties associated with a tracking information object and their names.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IComTrackingInfoProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IComTrackingInfoProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IComTrackingInfoProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a26bd3d-89e2-46fd-b9d1-b65ed12ae2ee">GetPropName</a>
</td>
<td align="left" width="63%">
Retrieves the name of the property corresponding to the specified index number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8036da8-3bd4-4500-a707-a43ac9dd5a52">PropCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of properties defined for a tracking information object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07f68734-a382-4fe5-86af-90805f61c68d">COM+ Instrumentation</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd179218(v=VS.85).aspx">COM+ Tracking</a>
 

 


---
UID: NN:sdoias.ISdoServiceControl
title: ISdoServiceControl (sdoias.h)
author: windows-sdk-content
description: Use the ISdoServiceControl interface to control the service being administered on the SDO computer.
old-location: nps\SDO_isdoservicecontrol.htm
tech.root: Nps
ms.assetid: c901ac9a-524a-498d-8b72-9afb26cf2c58
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISdoServiceControl, ISdoServiceControl interface [Network Policy Server], ISdoServiceControl interface [Network Policy Server],described, _sdo_isdoservicecontrol, nps.SDO_isdoservicecontrol, sdo.isdoservicecontrol, sdoias/ISdoServiceControl
ms.topic: interface
req.header: sdoias.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: SdoIas.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Iassdo.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Iassdo.dll
api_name:
 - ISdoServiceControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISdoServiceControl interface


## -description


Use the 
<b>ISdoServiceControl</b> interface to control the service being administered on the SDO computer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISdoServiceControl</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ISdoServiceControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISdoServiceControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdoservicecontrol-getservicestatus">GetServiceStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current status of the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdoservicecontrol-resetservice">ResetService</a>
</td>
<td align="left" width="63%">
Resets the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdoservicecontrol-startservice">StartService</a>
</td>
<td align="left" width="63%">
Starts the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdoservicecontrol-stopservice">StopService</a>
</td>
<td align="left" width="63%">
Stops the service.

</td>
</tr>
</table> 


## -remarks



Use the 
<a href="https://docs.microsoft.com/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo">ISdoMachine::GetServiceSDO</a> method to retrieve a pointer to an 
<b>ISdoServiceControl</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-server-data-objects-interfaces">Server Data Objects Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/Nps/sdo-server-data-objects-reference">Server Data Objects Reference</a>
 

 


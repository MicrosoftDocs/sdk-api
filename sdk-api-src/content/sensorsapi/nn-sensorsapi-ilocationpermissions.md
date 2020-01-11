---
UID: NN:sensorsapi.ILocationPermissions
title: ILocationPermissions (sensorsapi.h)
description: Provides the status of the system setting that allows users to change location settings.
old-location: winsensors\ilocationpermissions.htm
tech.root: SensorsAPI
ms.assetid: f4b46f4a-60be-4428-a4b5-6100ae3f1e1b
ms.date: 12/05/2018
ms.keywords: ILocationPermissions, ILocationPermissions interface [WinSensors], ILocationPermissions interface [WinSensors],described, sensorsapi/ILocationPermissions, winsensors.ilocationpermissions
f1_keywords:
- sensorsapi/ILocationPermissions
dev_langs:
- c++
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sensorsapi.dll
api_name:
- ILocationPermissions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILocationPermissions interface


## -description


Provides the status of the system setting that allows users to change location settings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILocationPermissions</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILocationPermissions</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILocationPermissions</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nf-sensorsapi-ilocationpermissions-getgloballocationpermission">GetGlobalLocationPermission</a>
</td>
<td align="left" width="63%">
Gets the status of the system setting that allows users to change location settings.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  <b>ILocationPermissions</b> is available in Windows 8.</div>
<div> </div>
For more information on location settings in Windows 8 see <a href="https://docs.microsoft.com/previous-versions/windows">Location settings</a>.




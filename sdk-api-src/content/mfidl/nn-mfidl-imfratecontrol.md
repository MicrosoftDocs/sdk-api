---
UID: NN:mfidl.IMFRateControl
title: IMFRateControl
author: windows-sdk-content
description: Gets or sets the playback rate.
old-location: mf\imfratecontrol.htm
old-project: medfound
ms.assetid: 54303c32-b260-4364-9130-a592694f2816
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 54303c32-b260-4364-9130-a592694f2816, IMFRateControl, IMFRateControl interface [Media Foundation], IMFRateControl interface [Media Foundation],described, mf.imfratecontrol, mfidl/IMFRateControl
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFSensorDeviceMode
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFRateControl
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFRateControl interface


## -description



          Gets or sets the playback rate.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFRateControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFRateControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFRateControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb970d06-0f82-4e35-8e03-68044c7f12cd">GetRate</a>
</td>
<td align="left" width="63%">
Gets the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/428d73fa-f284-4861-a41e-04ea7709db0f">SetRate</a>
</td>
<td align="left" width="63%">
Sets the current playback rate.

</td>
</tr>
</table> 


## -remarks



Objects can expose this interface as a service. To obtain a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier MF_RATE_CONTROL_SERVICE. The Media Session supports this interface. Media sources and transforms support this interface if they support rate changes. Media sinks do not need to support this interface. Media sinks are notified of rate changes through the <a href="https://msdn.microsoft.com/ba8afdf9-13eb-4e3d-b8a7-c74e0b40e998">IMFClockStateSink::OnClockSetRate</a> method.

For more information, see <a href="https://msdn.microsoft.com/509b2cc8-6017-41a9-ae80-9af21dce9367">About Rate Control</a>.

To discover the playback rates that an object supports, use the <a href="https://msdn.microsoft.com/a6c495fa-0f6a-4e4c-8fba-996b22d55053">IMFRateSupport</a> interface




## -see-also




<a href="https://msdn.microsoft.com/509b2cc8-6017-41a9-ae80-9af21dce9367">About Rate Control</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 


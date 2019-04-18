---
UID: NF:rtscom.IStylusPlugin.DataInterest
title: IStylusPlugin::DataInterest (rtscom.h)
author: windows-sdk-content
description: Retrieves the events for which the plug-in is to receive notifications.
old-location: tablet\istylusplugin_datainterest.htm
tech.root: tablet
ms.assetid: 7ff6ccf2-292c-4321-be2a-d6db7ce14943
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 7ff6ccf2-292c-4321-be2a-d6db7ce14943, DataInterest, DataInterest method [Tablet PC], DataInterest method [Tablet PC],IStylusPlugin interface, IStylusPlugin interface [Tablet PC],DataInterest method, IStylusPlugin.DataInterest, IStylusPlugin::DataInterest, rtscom/IStylusPlugin::DataInterest, tablet.istylusplugin_datainterest
ms.topic: method
req.header: rtscom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
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
req.dll: RTSCom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusPlugin.DataInterest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStylusPlugin::DataInterest


## -description



Retrieves the events for which the plug-in is to receive notifications.




## -parameters




### -param pDataInterest [out, retval]

The bitmask indicating the events for which the plug-in is to receive notifications.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The default is <b>RTSDI_None</b>.

The <a href="https://msdn.microsoft.com/f50cfafb-e709-4819-9e1a-679fbb54c7e0">RealTimeStylusDataInterest Enumeration</a> enumeration bitmask is retrieved every time a plug-in is enabled or disabled. The <b>DataInterest</b> mask of a plug-in is queried by the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object when the plug-in has been added to the plug-in collections.


#### Examples

The following C++ example implements a <b>IStylusPlugin::DataInterest Method</b> method that sets up a plug-in to receive <a href="https://msdn.microsoft.com/13fb831c-e3e8-4e04-81ce-d4658be105a0">IStylusPlugin::StylusDown Method</a>, <a href="https://msdn.microsoft.com/c6a3d563-4776-4ac6-bdc3-798192ba4546">IStylusPlugin::Packets Method</a>, <a href="https://msdn.microsoft.com/b0f9e49c-6a16-43c5-a653-d6142e58019a">IStylusPlugin::StylusUp Method</a>, <a href="https://msdn.microsoft.com/586e7fee-6340-46b6-941f-1316b2925e1c">IStylusPlugin::StylusInRange Method</a> and <a href="https://msdn.microsoft.com/236589f8-a6ae-4db3-8be4-68c5babeb9f0">IStylusPlugin::Error Method</a> notifications.


```cpp
STDMETHODIMP CPacketModifier::DataInterest( 
        /* [retval][out] */ RealTimeStylusDataInterest *pDataInterest)
{
	*pDataInterest = (RealTimeStylusDataInterest)(RTSDI_StylusDown | RTSDI_Packets | 
												  RTSDI_StylusUp | RTSDI_StylusInRange | 
												  RTSDI_Error);
	return S_OK;
}

```





## -see-also




<a href="https://msdn.microsoft.com/938e1eb2-3dd4-4e21-9c46-9ef840172b05">DynamicRenderer Class</a>



<a href="https://msdn.microsoft.com/1ea8359b-fc9f-4929-9499-c5017eb3d763">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>



<a href="https://msdn.microsoft.com/f50cfafb-e709-4819-9e1a-679fbb54c7e0">RealTimeStylusDataInterest Enumeration</a>
 

 


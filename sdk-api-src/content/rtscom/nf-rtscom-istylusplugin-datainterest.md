---
UID: NF:rtscom.IStylusPlugin.DataInterest
title: IStylusPlugin::DataInterest (rtscom.h)
description: Retrieves the events for which the plug-in is to receive notifications.
helpviewer_keywords: ["7ff6ccf2-292c-4321-be2a-d6db7ce14943","DataInterest","DataInterest method [Tablet PC]","DataInterest method [Tablet PC]","IStylusPlugin interface","IStylusPlugin interface [Tablet PC]","DataInterest method","IStylusPlugin.DataInterest","IStylusPlugin::DataInterest","rtscom/IStylusPlugin::DataInterest","tablet.istylusplugin_datainterest"]
old-location: tablet\istylusplugin_datainterest.htm
tech.root: tablet
ms.assetid: 7ff6ccf2-292c-4321-be2a-d6db7ce14943
ms.date: 12/05/2018
ms.keywords: 7ff6ccf2-292c-4321-be2a-d6db7ce14943, DataInterest, DataInterest method [Tablet PC], DataInterest method [Tablet PC],IStylusPlugin interface, IStylusPlugin interface [Tablet PC],DataInterest method, IStylusPlugin.DataInterest, IStylusPlugin::DataInterest, rtscom/IStylusPlugin::DataInterest, tablet.istylusplugin_datainterest
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStylusPlugin::DataInterest
 - rtscom/IStylusPlugin::DataInterest
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IStylusPlugin.DataInterest
---

# IStylusPlugin::DataInterest


## -description

Retrieves the events for which the plug-in is to receive notifications.

## -parameters

### -param pDataInterest [out, retval]

The bitmask indicating the events for which the plug-in is to receive notifications.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

The default is <b>RTSDI_None</b>.

The <a href="/windows/desktop/api/rtscom/ne-rtscom-realtimestylusdatainterest">RealTimeStylusDataInterest Enumeration</a> enumeration bitmask is retrieved every time a plug-in is enabled or disabled. The <b>DataInterest</b> mask of a plug-in is queried by the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object when the plug-in has been added to the plug-in collections.


#### Examples

The following C++ example implements a <b>IStylusPlugin::DataInterest Method</b> method that sets up a plug-in to receive <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusdown">IStylusPlugin::StylusDown Method</a>, <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-packets">IStylusPlugin::Packets Method</a>, <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusup">IStylusPlugin::StylusUp Method</a>, <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusinrange">IStylusPlugin::StylusInRange Method</a> and <a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-error">IStylusPlugin::Error Method</a> notifications.


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

<a href="/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-setdesiredpacketdescription">IRealTimeStylus::SetDesiredPacketDescription Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<a href="/windows/desktop/api/rtscom/ne-rtscom-realtimestylusdatainterest">RealTimeStylusDataInterest Enumeration</a>
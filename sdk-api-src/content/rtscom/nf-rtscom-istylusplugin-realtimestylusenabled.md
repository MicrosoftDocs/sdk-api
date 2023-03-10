---
UID: NF:rtscom.IStylusPlugin.RealTimeStylusEnabled
title: IStylusPlugin::RealTimeStylusEnabled (rtscom.h)
description: Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is enabled.
helpviewer_keywords: ["IStylusPlugin interface [Tablet PC]","RealTimeStylusEnabled method","IStylusPlugin.RealTimeStylusEnabled","IStylusPlugin::RealTimeStylusEnabled","RealTimeStylusEnabled","RealTimeStylusEnabled method [Tablet PC]","RealTimeStylusEnabled method [Tablet PC]","IStylusPlugin interface","bd5689c1-32e2-4a37-8dd2-4525b16f4662","rtscom/IStylusPlugin::RealTimeStylusEnabled","tablet.istylusplugin_realtimestylusenabled"]
old-location: tablet\istylusplugin_realtimestylusenabled.htm
tech.root: tablet
ms.assetid: bd5689c1-32e2-4a37-8dd2-4525b16f4662
ms.date: 12/05/2018
ms.keywords: IStylusPlugin interface [Tablet PC],RealTimeStylusEnabled method, IStylusPlugin.RealTimeStylusEnabled, IStylusPlugin::RealTimeStylusEnabled, RealTimeStylusEnabled, RealTimeStylusEnabled method [Tablet PC], RealTimeStylusEnabled method [Tablet PC],IStylusPlugin interface, bd5689c1-32e2-4a37-8dd2-4525b16f4662, rtscom/IStylusPlugin::RealTimeStylusEnabled, tablet.istylusplugin_realtimestylusenabled
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
 - IStylusPlugin::RealTimeStylusEnabled
 - rtscom/IStylusPlugin::RealTimeStylusEnabled
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
 - IStylusPlugin.RealTimeStylusEnabled
---

# IStylusPlugin::RealTimeStylusEnabled


## -description

Notifies the implementing plug-in that the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object is enabled.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

### -param cTcidCount [in]

Number of tablet context identifiers the RTS has encountered. Valid values are 0 through 8, inclusive.

### -param pTcids [in]

The tablet context identifiers.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

This method is called when the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has been enabled, or when a plug-in is added to a collection.


#### Examples

The following C++ example implements a <b>IStylusPlugin::RealTimeStylusEnabled Method</b> method that creates a new instance of an <a href="/windows/desktop/api/rtscom/nn-rtscom-istrokebuilder">IStrokeBuilder</a> object for the purpose of creating Ink strokes from packets collected by a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object.


```cpp
STDMETHODIMP CStrokeBuilderPlugin::RealTimeStylusEnabled( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ ULONG cTcidCount,
            /* [size_is][in] */ const TABLET_CONTEXT_ID *pTcids)
{
	// Create an IStrokeBuilder object
	return CoCreateInstance(CLSID_StrokeBuilder, NULL, CLSCTX_INPROC, IID_IStrokeBuilder, (VOID **)&m_pStrokeBuilder);
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-realtimestylusdisabled">IStylusPlugin::RealTimeStylusDisabled Method</a>
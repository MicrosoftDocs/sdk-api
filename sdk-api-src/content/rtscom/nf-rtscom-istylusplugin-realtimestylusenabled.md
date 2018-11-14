---
UID: NF:rtscom.IStylusPlugin.RealTimeStylusEnabled
title: IStylusPlugin::RealTimeStylusEnabled
author: windows-sdk-content
description: Notifies the implementing plug-in that the RealTimeStylus Class (RTS) object is enabled.
old-location: tablet\istylusplugin_realtimestylusenabled.htm
tech.root: tablet
ms.assetid: bd5689c1-32e2-4a37-8dd2-4525b16f4662
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IStylusPlugin interface [Tablet PC],RealTimeStylusEnabled method, IStylusPlugin.RealTimeStylusEnabled, IStylusPlugin::RealTimeStylusEnabled, RealTimeStylusEnabled, RealTimeStylusEnabled method [Tablet PC], RealTimeStylusEnabled method [Tablet PC],IStylusPlugin interface, bd5689c1-32e2-4a37-8dd2-4525b16f4662, rtscom/IStylusPlugin::RealTimeStylusEnabled, tablet.istylusplugin_realtimestylusenabled
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IStylusPlugin.RealTimeStylusEnabled
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rtscom.h
: 
- IStylusPlugin.RealTimeStylusEnabled
: 
---

# IStylusPlugin::RealTimeStylusEnabled


## -description



Notifies the implementing plug-in that the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object is enabled.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that sent the notification.


### -param cTcidCount [in]

Number of tablet context identifiers the RTS has encountered. Valid values are 0 through 8, inclusive.


### -param pTcids [in]

The tablet context identifiers.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is called when the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object has been enabled, or when a plug-in is added to a collection.


#### Examples

The following C++ example implements a <b>IStylusPlugin::RealTimeStylusEnabled Method</b> method that creates a new instance of an <a href="https://msdn.microsoft.com/309fcc8a-6a14-4ee3-b340-5e47ff249bf8">IStrokeBuilder</a> object for the purpose of creating Ink strokes from packets collected by a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CStrokeBuilderPlugin::RealTimeStylusEnabled( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ ULONG cTcidCount,
            /* [size_is][in] */ const TABLET_CONTEXT_ID *pTcids)
{
	// Create an IStrokeBuilder object
	return CoCreateInstance(CLSID_StrokeBuilder, NULL, CLSCTX_INPROC, IID_IStrokeBuilder, (VOID **)&amp;m_pStrokeBuilder);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/62425c21-62fb-4a29-b024-8d5dc237b430">IStylusPlugin::RealTimeStylusDisabled Method</a>
 

 


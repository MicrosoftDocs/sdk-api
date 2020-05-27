---
UID: NF:rtscom.IStylusPlugin.Error
title: IStylusPlugin::Error (rtscom.h)
description: Notifies the implementing object that this plug-in or one of the previous plug-ins in either the IStylusAsyncPlugin or IStylusSyncPlugin collection threw an exception.
helpviewer_keywords: ["236589f8-a6ae-4db3-8be4-68c5babeb9f0","Error","Error method [Tablet PC]","Error method [Tablet PC]","IStylusPlugin interface","IStylusPlugin interface [Tablet PC]","Error method","IStylusPlugin.Error","IStylusPlugin::Error","rtscom/IStylusPlugin::Error","tablet.istylusplugin_error"]
old-location: tablet\istylusplugin_error.htm
tech.root: tablet
ms.assetid: 236589f8-a6ae-4db3-8be4-68c5babeb9f0
ms.date: 12/05/2018
ms.keywords: 236589f8-a6ae-4db3-8be4-68c5babeb9f0, Error, Error method [Tablet PC], Error method [Tablet PC],IStylusPlugin interface, IStylusPlugin interface [Tablet PC],Error method, IStylusPlugin.Error, IStylusPlugin::Error, rtscom/IStylusPlugin::Error, tablet.istylusplugin_error
f1_keywords:
- rtscom/IStylusPlugin.Error
dev_langs:
- c++
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
- IStylusPlugin.Error
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStylusPlugin::Error


## -description



Notifies the implementing object that this plug-in or one of the previous plug-ins in either the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> or <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> collection threw an exception.




## -parameters




### -param piRtsSrc [in]

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param piPlugin [in]

The <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin</a> object that sent the notification.


### -param dataInterest [in]

Identifier of the <a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin</a> method that generated the error.


### -param hrErrorCode [in]

The <b>HRESULT</b> code for the error that occurred.


### -param lptrKey [in, out]

Used internally by the system.


## -returns



For a description of return values, see <a href="https://docs.microsoft.com/windows/desktop/tablet/classes-and-interfaces---ink-analysis">Classes and Interfaces - Ink Analysis</a>.




## -remarks



This method is called when the RTS object has caught an exception.


#### Examples

The following C++ example implements an <b>IStylusPlugin::Error Method</b> method that outputs a message and error code to the debug window using <a href="https://msdn2.microsoft.com/library/4wyz8787.aspx">The TRACE Macro</a>.


```cpp
STDMETHODIMP CPacketModifier::Error( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ IStylusPlugin *piPlugin,
            /* [in] */ RealTimeStylusDataInterest dataInterest,
            /* [in] */ HRESULT hrErrorCode,
            /* [out][in] */ LONG_PTR *lptrKey)
{
	CString strError;
	strError.Format(L"An error occurred. Error code: %d", hrErrorCode);
	TRACE(strError);
	return S_OK;
}

```





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)">DynamicRenderer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-datainterest">IStylusPlugin::DataInterest Method</a>
 

 


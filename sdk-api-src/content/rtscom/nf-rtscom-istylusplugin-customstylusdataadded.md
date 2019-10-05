---
UID: NF:rtscom.IStylusPlugin.CustomStylusDataAdded
title: IStylusPlugin::CustomStylusDataAdded (rtscom.h)
author: windows-sdk-content
description: Notifies the implementing plug-in that custom stylus data is available.
old-location: tablet\istylusplugin_customstylusdataadded.htm
tech.root: tablet
ms.assetid: 0d3f556c-b0a8-4346-b7da-82f1a3c2603c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 0d3f556c-b0a8-4346-b7da-82f1a3c2603c, CustomStylusDataAdded, CustomStylusDataAdded method [Tablet PC], CustomStylusDataAdded method [Tablet PC],IStylusPlugin interface, IStylusPlugin interface [Tablet PC],CustomStylusDataAdded method, IStylusPlugin.CustomStylusDataAdded, IStylusPlugin::CustomStylusDataAdded, rtscom/IStylusPlugin::CustomStylusDataAdded, tablet.istylusplugin_customstylusdataadded
ms.topic: method
f1_keywords: 
 - "rtscom/IStylusPlugin.CustomStylusDataAdded"
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
 - IStylusPlugin.CustomStylusDataAdded
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStylusPlugin::CustomStylusDataAdded


## -description



Notifies the implementing plug-in that custom stylus data is available.




## -parameters




### -param piRtsSrc [in]

The <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param pGuidId [in]

The globally unique identifier (GUID) for the custom data.


### -param cbData [in]

The size, in chars, of the buffer, <i>pbData</i>. Valid values are 0 through 0x7FFF, inclusive.


### -param pbData [in]

A pointer to the buffer containing the custom data sent by the RTS object.


## -returns



For a description of return values, see <a href="https://docs.microsoft.com/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is called when <b>IStylusPlugin::CustomStylusDataAdded Method</b> is being processed. The custom data is passed in the <i>pbData</i> member, with a GUID in the <i>pGuidId</i> member to pass type information. This class cannot be inherited.


#### Examples

The following C++ code example implements a <b>IStylusPlugin::CustomStylusDataAdded Method</b> method that handles the data from a gesture event and sets a static text control, <code>m_pStatusControl</code>, to a string representation of the gesture data.


```cpp
STDMETHODIMP CGestureHandler::CustomStylusDataAdded( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ const GUID *pGuidId,
            /* [in] */ ULONG cbData,
            /* [in] */ const BYTE *pbData)
{
	// Did we get passed gesture data?
	if (*pGuidId == GUID_GESTURE_DATA)
	{
		// Another way to check for gestures is to see if the data
		// is the right size and actually points to something
		if ((cbData == sizeof(GESTURE_DATA)) && (pbData != NULL))
		{
			// Access the data coming as a GESTURE_DATA structure
			GESTURE_DATA* pGD = (GESTURE_DATA*)pbData;

			CString strStatus;
			CString strGestureId;
			
			// Helper function that maps the gesture ID to a string value
			SetGestureString(pGD->gestureId, &strGestureId);

			strStatus.Format(L"Gesture=%s\tConfidence=%d\tStrokes=%d", strGestureId, pGD->recoConfidence, pGD->strokeCount);
			m_pStatusControl->SetWindowTextW(strStatus);
		}
		else
		{
			m_pStatusControl->SetWindowTextW(L"Not gesture data.");
		}
	}
	else
	{
		m_pStatusControl->SetWindowTextW(L"Not gesture data.");
	}

	return S_OK;
}

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer Class</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-igesturerecognizer">IGestureRecognizer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>
 

 


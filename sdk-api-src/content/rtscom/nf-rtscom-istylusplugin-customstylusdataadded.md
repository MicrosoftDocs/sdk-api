---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IStylusPlugin::CustomStylusDataAdded


## -description



Notifies the implementing plug-in that custom stylus data is available.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> (RTS) object that sent the notification.


### -param pGuidId [in]

The globally unique identifier (GUID) for the custom data.


### -param cbData [in]

The size, in chars, of the buffer, <i>pbData</i>. Valid values are 0 through 0x7FFF, inclusive.


### -param pbData [in]

A pointer to the buffer containing the custom data sent by the RTS object.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



This method is called when <b>IStylusPlugin::CustomStylusDataAdded Method</b> is being processed. The custom data is passed in the <i>pbData</i> member, with a GUID in the <i>pGuidId</i> member to pass type information. This class cannot be inherited.


#### Examples

The following C++ code example implements a <b>IStylusPlugin::CustomStylusDataAdded Method</b> method that handles the data from a gesture event and sets a static text control, <code>m_pStatusControl</code>, to a string representation of the gesture data.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CGestureHandler::CustomStylusDataAdded( 
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
		if ((cbData == sizeof(GESTURE_DATA)) &amp;&amp; (pbData != NULL))
		{
			// Access the data coming as a GESTURE_DATA structure
			GESTURE_DATA* pGD = (GESTURE_DATA*)pbData;

			CString strStatus;
			CString strGestureId;
			
			// Helper function that maps the gesture ID to a string value
			SetGestureString(pGD-&gt;gestureId, &amp;strGestureId);

			strStatus.Format(L"Gesture=%s\tConfidence=%d\tStrokes=%d", strGestureId, pGD-&gt;recoConfidence, pGD-&gt;strokeCount);
			m_pStatusControl-&gt;SetWindowTextW(strStatus);
		}
		else
		{
			m_pStatusControl-&gt;SetWindowTextW(L"Not gesture data.");
		}
	}
	else
	{
		m_pStatusControl-&gt;SetWindowTextW(L"Not gesture data.");
	}

	return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer Class</a>



<a href="https://msdn.microsoft.com/dfdc00d6-c843-4298-9773-92775406fbf7">IGestureRecognizer Interface</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 


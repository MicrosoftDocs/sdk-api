---
UID: NF:rtscom.IStylusPlugin.StylusInRange
title: IStylusPlugin::StylusInRange (rtscom.h)
description: Notifies the implementing plug-in that the stylus is entering the detection range of the digitizer.
helpviewer_keywords: ["586e7fee-6340-46b6-941f-1316b2925e1c","IStylusPlugin interface [Tablet PC]","StylusInRange method","IStylusPlugin.StylusInRange","IStylusPlugin::StylusInRange","StylusInRange","StylusInRange method [Tablet PC]","StylusInRange method [Tablet PC]","IStylusPlugin interface","rtscom/IStylusPlugin::StylusInRange","tablet.istylusplugin_stylusinrange"]
old-location: tablet\istylusplugin_stylusinrange.htm
tech.root: tablet
ms.assetid: 586e7fee-6340-46b6-941f-1316b2925e1c
ms.date: 12/05/2018
ms.keywords: 586e7fee-6340-46b6-941f-1316b2925e1c, IStylusPlugin interface [Tablet PC],StylusInRange method, IStylusPlugin.StylusInRange, IStylusPlugin::StylusInRange, StylusInRange, StylusInRange method [Tablet PC], StylusInRange method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::StylusInRange, tablet.istylusplugin_stylusinrange
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
 - IStylusPlugin::StylusInRange
 - rtscom/IStylusPlugin::StylusInRange
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
 - IStylusPlugin.StylusInRange
---

# IStylusPlugin::StylusInRange


## -description

Notifies the implementing plug-in that the stylus is entering the detection range of the digitizer.

## -parameters

### -param piRtsSrc [in]

The <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object that sent the notification.

### -param tcid [in]

Tablet context identifier.

### -param sid [in]

Stylus identifier.

## -returns

For a description of return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

The stylus is in range of the digitizer. This is a good place to check if the stylus is inverted and if so, switch to eraser mode.


#### Examples

The following C++ example implements a <b>IStylusPlugin::StylusInRange Method</b> method that gets the status of all the buttons on a stylus and reports them to the debug window using the <a href="/previous-versions/visualstudio/visual-studio-2010/4wyz8787(v=vs.100)">TRACE</a> macro.


```cpp
STDMETHODIMP CPacketModifier::StylusInRange( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ TABLET_CONTEXT_ID tcid,
            /* [in] */ STYLUS_ID sid)
{
    IInkCursor* pInkCursor;
	HRESULT hr = piRtsSrc->GetStylusForId(sid, &pInkCursor);

	if (SUCCEEDED(hr))
	{
		IInkCursorButtons* pInkCursorButtons;
		hr = pInkCursor->get_Buttons(&pInkCursorButtons);

		if (SUCCEEDED(hr))
		{
			LONG lButtonCount;
			pInkCursorButtons->get_Count(&lButtonCount);

			if (SUCCEEDED(hr))
			{
				IInkCursorButton* pInkCursorButton;
				VARIANT index;
				VariantInit(&index);
				index.vt = VT_I4;

				for (index.intVal = 0; index.intVal < lButtonCount; index.intVal++)
				{
					hr = pInkCursorButtons->Item(index, &pInkCursorButton);

					if (SUCCEEDED(hr))
					{
						InkCursorButtonState currentState;
						hr = pInkCursorButton->get_State(&currentState);

						if (SUCCEEDED(hr))
						{
							switch(currentState)
							{
								case ICBS_Unavailable:
									TRACE("ICBS_Unavailable\n");
									break;

								case ICBS_Up:
									TRACE("ICBS_Up\n");
									break;

								case ICBS_Down:
									TRACE("ICBS_Down\n");
									break;

								default:
									TRACE("Cursor button state unknown.\n");
									break;
							}
						}
					}
				}

				VariantClear(&index);
			}
		}
	}

	return hr;
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusplugin">IStylusPlugin Interface</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-istylusplugin-stylusoutofrange">IStylusPlugin::StylusOutOfRange Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>
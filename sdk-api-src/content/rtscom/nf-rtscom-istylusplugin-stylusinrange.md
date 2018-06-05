---
UID: NF:rtscom.IStylusPlugin.StylusInRange
title: IStylusPlugin::StylusInRange
author: windows-sdk-content
description: Notifies the implementing plug-in that the stylus is entering the detection range of the digitizer.
old-location: tablet\istylusplugin_stylusinrange.htm
old-project: tablet
ms.assetid: 586e7fee-6340-46b6-941f-1316b2925e1c
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 586e7fee-6340-46b6-941f-1316b2925e1c, IStylusPlugin interface [Tablet PC],StylusInRange method, IStylusPlugin.StylusInRange, IStylusPlugin::StylusInRange, StylusInRange, StylusInRange method [Tablet PC], StylusInRange method [Tablet PC],IStylusPlugin interface, rtscom/IStylusPlugin::StylusInRange, tablet.istylusplugin_stylusinrange
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: StylusQueue
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RTSCom.dll
api_name:
-	IStylusPlugin.StylusInRange
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStylusPlugin::StylusInRange


## -description



Notifies the implementing plug-in that the stylus is entering the detection range of the digitizer.




## -parameters




### -param piRtsSrc [in]

The <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object that sent the notification.


### -param tcid [in]

Tablet context identifier.


### -param sid [in]

Stylus identifier.


## -returns



For a description of return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



The stylus is in range of the digitizer. This is a good place to check if the stylus is inverted and if so, switch to eraser mode.


#### Examples

The following C++ example implements a <b>IStylusPlugin::StylusInRange Method</b> method that gets the status of all the buttons on a stylus and reports them to the debug window using the <a href="http://go.microsoft.com/fwlink/p/?linkid=73729">TRACE</a> macro.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CPacketModifier::StylusInRange( 
            /* [in] */ IRealTimeStylus *piRtsSrc,
            /* [in] */ TABLET_CONTEXT_ID tcid,
            /* [in] */ STYLUS_ID sid)
{
    IInkCursor* pInkCursor;
	HRESULT hr = piRtsSrc-&gt;GetStylusForId(sid, &amp;pInkCursor);

	if (SUCCEEDED(hr))
	{
		IInkCursorButtons* pInkCursorButtons;
		hr = pInkCursor-&gt;get_Buttons(&amp;pInkCursorButtons);

		if (SUCCEEDED(hr))
		{
			LONG lButtonCount;
			pInkCursorButtons-&gt;get_Count(&amp;lButtonCount);

			if (SUCCEEDED(hr))
			{
				IInkCursorButton* pInkCursorButton;
				VARIANT index;
				VariantInit(&amp;index);
				index.vt = VT_I4;

				for (index.intVal = 0; index.intVal &lt; lButtonCount; index.intVal++)
				{
					hr = pInkCursorButtons-&gt;Item(index, &amp;pInkCursorButton);

					if (SUCCEEDED(hr))
					{
						InkCursorButtonState currentState;
						hr = pInkCursorButton-&gt;get_State(&amp;currentState);

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

				VariantClear(&amp;index);
			}
		}
	}

	return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/bbef5cdb-4112-4733-80bb-692b7a198605">IStylusPlugin Interface</a>



<a href="https://msdn.microsoft.com/fd662c32-c226-4dbb-807a-3e560452ef15">IStylusPlugin::StylusOutOfRange Method</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>
 

 


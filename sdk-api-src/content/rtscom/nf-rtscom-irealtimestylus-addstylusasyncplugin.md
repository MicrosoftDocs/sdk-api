---
UID: NF:rtscom.IRealTimeStylus.AddStylusAsyncPlugin
title: IRealTimeStylus::AddStylusAsyncPlugin (rtscom.h)
description: Adds an IStylusAsyncPlugin to the asynchronous plug-in collection at the specified index.
helpviewer_keywords: ["AddStylusAsyncPlugin","AddStylusAsyncPlugin method [Tablet PC]","AddStylusAsyncPlugin method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","AddStylusAsyncPlugin method","IRealTimeStylus.AddStylusAsyncPlugin","IRealTimeStylus::AddStylusAsyncPlugin","fc22fa79-469a-47f0-96ce-9a041fc8a617","rtscom/IRealTimeStylus::AddStylusAsyncPlugin","tablet.irealtimestylus_addstylusasyncplugin"]
old-location: tablet\irealtimestylus_addstylusasyncplugin.htm
tech.root: tablet
ms.assetid: fc22fa79-469a-47f0-96ce-9a041fc8a617
ms.date: 12/05/2018
ms.keywords: AddStylusAsyncPlugin, AddStylusAsyncPlugin method [Tablet PC], AddStylusAsyncPlugin method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],AddStylusAsyncPlugin method, IRealTimeStylus.AddStylusAsyncPlugin, IRealTimeStylus::AddStylusAsyncPlugin, fc22fa79-469a-47f0-96ce-9a041fc8a617, rtscom/IRealTimeStylus::AddStylusAsyncPlugin, tablet.irealtimestylus_addstylusasyncplugin
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
 - IRealTimeStylus::AddStylusAsyncPlugin
 - rtscom/IRealTimeStylus::AddStylusAsyncPlugin
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
 - IRealTimeStylus.AddStylusAsyncPlugin
---

# IRealTimeStylus::AddStylusAsyncPlugin


## -description

Adds an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> to the asynchronous plug-in collection at the specified index.

## -parameters

### -param iIndex [in]

Specifies the index of the plug-in in the asynchronous plug-in collection.

### -param piPlugin [in]

The plug-in to add to.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

You cannot add asynchronous plug-ins if <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object has a child <b>RealTimeStylus Class</b> object.


#### Examples

The following C++ code example adds an instance of an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a> to a <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus</a> object. The example code uses the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on a <a href="/windows/desktop/tablet/gesturerecognizer-class">GestureRecognizer</a> plug-in, <code>g_pGestureHandler</code>, to get the <b>IStylusAsyncPlugin</b> interface, then calls <b>IRealTimeStylus::AddStylusAsyncPlugin Method</b>.


```cpp
HRESULT CCOMRTSDlg::InitGestureHandler()
{
	// Create an IGestureHandler object
	HRESULT hr = CoCreateInstance(CLSID_GestureHandler, NULL, CLSCTX_INPROC, IID_IGestureHandler, (VOID **)&g_pGestureHandler);

	if (SUCCEEDED(hr))
	{
		// Get a pointer to the IStylusAsyncPlugin interface
		IStylusAsyncPlugin* pAsyncPlugin;
		hr = g_pGestureHandler->QueryInterface(IID_IStylusAsyncPlugin, reinterpret_cast<void**>(&pAsyncPlugin));
		
		if (SUCCEEDED(hr))
		{
			// Get the current count of plugins so we can
			// add this one to the end of the collection
			ULONG nAsyncPluginCount;
			hr = g_pRealTimeStylus->GetStylusAsyncPluginCount(&nAsyncPluginCount);

			if (SUCCEEDED(hr))
			{
				// Add the plugin to the StylusAsyncPlugin collection
				hr = g_pRealTimeStylus->AddStylusAsyncPlugin(nAsyncPluginCount, pAsyncPlugin);

				if (SUCCEEDED(hr))
				{
					// Pass the Gesture Handler a pointer to the 
					// status window so it can update the status
					hr = g_pGestureHandler->SetStatusWindow(&m_staticGestureStatus);
				}
			}
		}
	}
	return hr;
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a>



<b>RealTimeStylus Class</b>
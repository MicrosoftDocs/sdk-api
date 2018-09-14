---
UID: NF:rtscom.IRealTimeStylus.AddStylusAsyncPlugin
title: IRealTimeStylus::AddStylusAsyncPlugin
author: windows-sdk-content
description: Adds an IStylusAsyncPlugin to the asynchronous plug-in collection at the specified index.
old-location: tablet\irealtimestylus_addstylusasyncplugin.htm
tech.root: tablet
ms.assetid: fc22fa79-469a-47f0-96ce-9a041fc8a617
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: AddStylusAsyncPlugin, AddStylusAsyncPlugin method [Tablet PC], AddStylusAsyncPlugin method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],AddStylusAsyncPlugin method, IRealTimeStylus.AddStylusAsyncPlugin, IRealTimeStylus::AddStylusAsyncPlugin, fc22fa79-469a-47f0-96ce-9a041fc8a617, rtscom/IRealTimeStylus::AddStylusAsyncPlugin, tablet.irealtimestylus_addstylusasyncplugin
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
 - IRealTimeStylus.AddStylusAsyncPlugin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRealTimeStylus::AddStylusAsyncPlugin


## -description


Adds an <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> to the asynchronous plug-in collection at the specified index.
        


## -parameters




### -param iIndex [in]

Specifies the index of the plug-in in the asynchronous plug-in collection.


### -param piPlugin [in]

The plug-in to add to.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



You cannot add asynchronous plug-ins if <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object has a child <b>RealTimeStylus Class</b> object.


#### Examples

The following C++ code example adds an instance of an <a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a> to a <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus</a> object. The example code uses the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> method on a <a href="https://msdn.microsoft.com/7cdaf3bf-7aae-4d36-af1c-0eb5a726f388">GestureRecognizer</a> plug-in, <code>g_pGestureHandler</code>, to get the <b>IStylusAsyncPlugin</b> interface, then calls <b>IRealTimeStylus::AddStylusAsyncPlugin Method</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CCOMRTSDlg::InitGestureHandler()
{
	// Create an IGestureHandler object
	HRESULT hr = CoCreateInstance(CLSID_GestureHandler, NULL, CLSCTX_INPROC, IID_IGestureHandler, (VOID **)&amp;g_pGestureHandler);

	if (SUCCEEDED(hr))
	{
		// Get a pointer to the IStylusAsyncPlugin interface
		IStylusAsyncPlugin* pAsyncPlugin;
		hr = g_pGestureHandler-&gt;QueryInterface(IID_IStylusAsyncPlugin, reinterpret_cast&lt;void**&gt;(&amp;pAsyncPlugin));
		
		if (SUCCEEDED(hr))
		{
			// Get the current count of plugins so we can
			// add this one to the end of the collection
			ULONG nAsyncPluginCount;
			hr = g_pRealTimeStylus-&gt;GetStylusAsyncPluginCount(&amp;nAsyncPluginCount);

			if (SUCCEEDED(hr))
			{
				// Add the plugin to the StylusAsyncPlugin collection
				hr = g_pRealTimeStylus-&gt;AddStylusAsyncPlugin(nAsyncPluginCount, pAsyncPlugin);

				if (SUCCEEDED(hr))
				{
					// Pass the Gesture Handler a pointer to the 
					// status window so it can update the status
					hr = g_pGestureHandler-&gt;SetStatusWindow(&amp;m_staticGestureStatus);
				}
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




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a>



<b>RealTimeStylus Class</b>
 

 


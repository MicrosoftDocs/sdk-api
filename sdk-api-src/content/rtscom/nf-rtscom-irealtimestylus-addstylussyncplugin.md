---
UID: NF:rtscom.IRealTimeStylus.AddStylusSyncPlugin
title: IRealTimeStylus::AddStylusSyncPlugin
author: windows-sdk-content
description: Adds an IStylusSyncPlugin to the synchronous plug-in collection at the specified index.
old-location: tablet\irealtimestylus_addstylussyncplugin.htm
old-project: tablet
ms.assetid: db38e39a-27ba-42ca-8748-b5e9c4db18f7
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: AddStylusSyncPlugin, AddStylusSyncPlugin method [Tablet PC], AddStylusSyncPlugin method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],AddStylusSyncPlugin method, IRealTimeStylus.AddStylusSyncPlugin, IRealTimeStylus::AddStylusSyncPlugin, db38e39a-27ba-42ca-8748-b5e9c4db18f7, rtscom/IRealTimeStylus::AddStylusSyncPlugin, tablet.irealtimestylus_addstylussyncplugin
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RTSCom.dll
api_name:
 - IRealTimeStylus.AddStylusSyncPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IRealTimeStylus::AddStylusSyncPlugin


## -description



Adds an <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> to the synchronous plug-in collection at the specified index.




## -parameters




### -param iIndex [in]

The index of the synchronous plug-in collection where the plug-in is added.


### -param piPlugin [in]

The plug-in that is added.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Use this to dynamically add a plug-in to the synchronous plug-in collection.

The synchronous and asynchronous plug-in collections on the <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> object can be modified without disabling and then re-enabling the <b>RealTimeStylus Class</b> object.

Plugins must aggregate the free threaded marshaler and must not be single threaded apartment objects.


#### Examples

The following C++ code example implements an event handler for a <b>CheckBox Control (Windows Forms)</b>. Depending on the checked state of the control, represented by the <code>m_btnPacketFilter</code> member variable, the function either adds or removes the plug-in represented by the global <code>g_pPacketModifier</code> variable.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void CCOMRTSDlg::OnBnClickedCheckPacketFilter()
{
	HRESULT hr;
	IStylusSyncPlugin* pSyncPlugin;

	hr = g_pPacketModifier-&gt;QueryInterface(IID_IStylusSyncPlugin, reinterpret_cast&lt;void**&gt;(&amp;pSyncPlugin));

	if (SUCCEEDED(hr))
	{
		if (m_btnPacketFilter.GetCheck())
		{
			// If the checkbox is checked, add the 
			// Packet Modifier plugin to the RealTimeStylus
			hr = g_pRealTimeStylus-&gt;AddStylusSyncPlugin(0, pSyncPlugin);
		}
		else
		{
			// If the checkbox is not checked, remove the 
			// Packet Modifier plugin from the RealTimeStylus
			hr = g_pRealTimeStylus-&gt;RemoveStylusSyncPlugin(0, &amp;pSyncPlugin);
		}
	}
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bfd13012-decf-423a-bc1a-39fb9b0eb64e">IRealTimeStylus</a>



<a href="https://msdn.microsoft.com/fc22fa79-469a-47f0-96ce-9a041fc8a617">IRealTimeStylus::AddStylusAsyncPlugin Method</a>



<b>RealTimeStylus Class</b>
 

 


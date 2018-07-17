---
UID: NF:rtscom.IRealTimeStylus.RemoveStylusSyncPlugin
title: IRealTimeStylus::RemoveStylusSyncPlugin
author: windows-sdk-content
description: Removes an IStylusSyncPlugin from the collection at the specified index.
old-location: tablet\irealtimestylus_removestylussyncplugin.htm
old-project: tablet
ms.assetid: 5f04dc8a-c0f5-47fd-a814-490e1dfe2cf8
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 5f04dc8a-c0f5-47fd-a814-490e1dfe2cf8, IRealTimeStylus interface [Tablet PC],RemoveStylusSyncPlugin method, IRealTimeStylus.RemoveStylusSyncPlugin, IRealTimeStylus::RemoveStylusSyncPlugin, RemoveStylusSyncPlugin, RemoveStylusSyncPlugin method [Tablet PC], RemoveStylusSyncPlugin method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::RemoveStylusSyncPlugin, tablet.irealtimestylus_removestylussyncplugin
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
 - IRealTimeStylus.RemoveStylusSyncPlugin
product: Windows
targetos: Windows
req.lib: 
req.dll: RTSCom.dll
req.irql: 
req.product: ADAM
---

# IRealTimeStylus::RemoveStylusSyncPlugin


## -description



Removes an <a href="https://msdn.microsoft.com/e3e02d5a-a004-49de-b2d8-86ccfc120481">IStylusSyncPlugin</a> from the collection at the specified index.




## -parameters




### -param iIndex [in]

The index of the plug-in to be removed.


### -param ppiPlugin [in, out]

A pointer to the plug-in to remove. If you are not interested in receiving the pointer to the removed plug-in, pass <b>NULL</b> for this parameter.


## -returns



For a description of the return values, see <a href="https://msdn.microsoft.com/fc0900b4-f08b-4a93-bbc0-d3db067d7917">RealTimeStylus Classes and Interfaces</a>.




## -remarks



Use to dynamically remove a specific plug-in from the synchronous plug-in collection.

The synchronous and asynchronous plug-in collections on <a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a> can be modified without disabling and then re-enabling <b>RealTimeStylus Class</b>.


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



<a href="https://msdn.microsoft.com/9c993147-3711-45ad-8996-e1434fd4b657">IRealTimeStylus::RemoveStylusAsyncPlugin Method</a>



<a href="https://msdn.microsoft.com/bf961d70-2576-493b-a34d-c7c72b6c0234">IStylusAsyncPlugin</a>



<a href="https://msdn.microsoft.com/fd686a78-b0a8-41d2-a37b-90544f531270">RealTimeStylus Class</a>
 

 


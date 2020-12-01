---
UID: NF:rtscom.IRealTimeStylus.RemoveStylusSyncPlugin
title: IRealTimeStylus::RemoveStylusSyncPlugin (rtscom.h)
description: Removes an IStylusSyncPlugin from the collection at the specified index.
helpviewer_keywords: ["5f04dc8a-c0f5-47fd-a814-490e1dfe2cf8","IRealTimeStylus interface [Tablet PC]","RemoveStylusSyncPlugin method","IRealTimeStylus.RemoveStylusSyncPlugin","IRealTimeStylus::RemoveStylusSyncPlugin","RemoveStylusSyncPlugin","RemoveStylusSyncPlugin method [Tablet PC]","RemoveStylusSyncPlugin method [Tablet PC]","IRealTimeStylus interface","rtscom/IRealTimeStylus::RemoveStylusSyncPlugin","tablet.irealtimestylus_removestylussyncplugin"]
old-location: tablet\irealtimestylus_removestylussyncplugin.htm
tech.root: tablet
ms.assetid: 5f04dc8a-c0f5-47fd-a814-490e1dfe2cf8
ms.date: 12/05/2018
ms.keywords: 5f04dc8a-c0f5-47fd-a814-490e1dfe2cf8, IRealTimeStylus interface [Tablet PC],RemoveStylusSyncPlugin method, IRealTimeStylus.RemoveStylusSyncPlugin, IRealTimeStylus::RemoveStylusSyncPlugin, RemoveStylusSyncPlugin, RemoveStylusSyncPlugin method [Tablet PC], RemoveStylusSyncPlugin method [Tablet PC],IRealTimeStylus interface, rtscom/IRealTimeStylus::RemoveStylusSyncPlugin, tablet.irealtimestylus_removestylussyncplugin
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
 - IRealTimeStylus::RemoveStylusSyncPlugin
 - rtscom/IRealTimeStylus::RemoveStylusSyncPlugin
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
 - IRealTimeStylus.RemoveStylusSyncPlugin
---

# IRealTimeStylus::RemoveStylusSyncPlugin


## -description

Removes an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> from the collection at the specified index.

## -parameters

### -param iIndex [in]

The index of the plug-in to be removed.

### -param ppiPlugin [in, out]

A pointer to the plug-in to remove. If you are not interested in receiving the pointer to the removed plug-in, pass <b>NULL</b> for this parameter.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Use to dynamically remove a specific plug-in from the synchronous plug-in collection.

The synchronous and asynchronous plug-in collections on <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> can be modified without disabling and then re-enabling <b>RealTimeStylus Class</b>.


#### Examples

The following C++ code example implements an event handler for a <b>CheckBox Control (Windows Forms)</b>. Depending on the checked state of the control, represented by the <code>m_btnPacketFilter</code> member variable, the function either adds or removes the plug-in represented by the global <code>g_pPacketModifier</code> variable.


```cpp
void CCOMRTSDlg::OnBnClickedCheckPacketFilter()
{
	HRESULT hr;
	IStylusSyncPlugin* pSyncPlugin;

	hr = g_pPacketModifier->QueryInterface(IID_IStylusSyncPlugin, reinterpret_cast<void**>(&pSyncPlugin));

	if (SUCCEEDED(hr))
	{
		if (m_btnPacketFilter.GetCheck())
		{
			// If the checkbox is checked, add the 
			// Packet Modifier plugin to the RealTimeStylus
			hr = g_pRealTimeStylus->AddStylusSyncPlugin(0, pSyncPlugin);
		}
		else
		{
			// If the checkbox is not checked, remove the 
			// Packet Modifier plugin from the RealTimeStylus
			hr = g_pRealTimeStylus->RemoveStylusSyncPlugin(0, &pSyncPlugin);
		}
	}
}

```

## -see-also

<a href="/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus">IRealTimeStylus</a>



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-removestylusasyncplugin">IRealTimeStylus::RemoveStylusAsyncPlugin Method</a>



<a href="/windows/desktop/api/rtscom/nn-rtscom-istylusasyncplugin">IStylusAsyncPlugin</a>



<a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a>
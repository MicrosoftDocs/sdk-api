---
UID: NF:rtscom.IRealTimeStylus.AddStylusSyncPlugin
title: IRealTimeStylus::AddStylusSyncPlugin (rtscom.h)
description: Adds an IStylusSyncPlugin to the synchronous plug-in collection at the specified index.
helpviewer_keywords: ["AddStylusSyncPlugin","AddStylusSyncPlugin method [Tablet PC]","AddStylusSyncPlugin method [Tablet PC]","IRealTimeStylus interface","IRealTimeStylus interface [Tablet PC]","AddStylusSyncPlugin method","IRealTimeStylus.AddStylusSyncPlugin","IRealTimeStylus::AddStylusSyncPlugin","db38e39a-27ba-42ca-8748-b5e9c4db18f7","rtscom/IRealTimeStylus::AddStylusSyncPlugin","tablet.irealtimestylus_addstylussyncplugin"]
old-location: tablet\irealtimestylus_addstylussyncplugin.htm
tech.root: tablet
ms.assetid: db38e39a-27ba-42ca-8748-b5e9c4db18f7
ms.date: 12/05/2018
ms.keywords: AddStylusSyncPlugin, AddStylusSyncPlugin method [Tablet PC], AddStylusSyncPlugin method [Tablet PC],IRealTimeStylus interface, IRealTimeStylus interface [Tablet PC],AddStylusSyncPlugin method, IRealTimeStylus.AddStylusSyncPlugin, IRealTimeStylus::AddStylusSyncPlugin, db38e39a-27ba-42ca-8748-b5e9c4db18f7, rtscom/IRealTimeStylus::AddStylusSyncPlugin, tablet.irealtimestylus_addstylussyncplugin
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
 - IRealTimeStylus::AddStylusSyncPlugin
 - rtscom/IRealTimeStylus::AddStylusSyncPlugin
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
 - IRealTimeStylus.AddStylusSyncPlugin
---

# IRealTimeStylus::AddStylusSyncPlugin


## -description

Adds an <a href="/windows/desktop/api/rtscom/nn-rtscom-istylussyncplugin">IStylusSyncPlugin</a> to the synchronous plug-in collection at the specified index.

## -parameters

### -param iIndex [in]

The index of the synchronous plug-in collection where the plug-in is added.

### -param piPlugin [in]

The plug-in that is added.

## -returns

For a description of the return values, see <a href="/windows/desktop/tablet/realtimestylus-classes-and-interfaces">RealTimeStylus Classes and Interfaces</a>.

## -remarks

Use this to dynamically add a plug-in to the synchronous plug-in collection.

The synchronous and asynchronous plug-in collections on the <a href="/windows/desktop/tablet/realtimestylus-class">RealTimeStylus Class</a> object can be modified without disabling and then re-enabling the <b>RealTimeStylus Class</b> object.

Plugins must aggregate the free threaded marshaler and must not be single threaded apartment objects.


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



<a href="/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus-addstylusasyncplugin">IRealTimeStylus::AddStylusAsyncPlugin Method</a>



<b>RealTimeStylus Class</b>